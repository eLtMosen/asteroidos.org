Catfish (Mobvoi Ticwatch Pro), catfish-ext (Ticwatch Pro 2020) and Catshark (Ticwatch Pro 4G/LTE) are a series of feature-complete round watches with a secondary display for timekeeping. The port is mostly complete, but work is still needed to get the LCD fully supported and to expose all its functions.
Warning: Ticwatch Pro 3 series are not supported at the moment. If you would like to help with a porting effort for these, please contact us on the matrix chat.

<div class="support-row">
  <div class="support-col">Display<div class="support-col-good"></div></div>
  <div class="support-col">Touch<div class="support-col-good"></div></div>
  <div class="support-col">Microphone<div class="support-col-bad"></div></div>
  <div class="support-col">Bluetooth<div class="support-col-good"></div></div>
  <div class="support-col">Haptics<div class="support-col-good"></div></div>
  <div class="support-col">USB<div class="support-col-good"></div></div>
  <div class="support-col">WLAN<div class="support-col-good"></div></div>
  <div class="support-col">Heart Rate<div class="support-col-good"></div></div>
  <div class="support-col">Tilt-to-Wake<div class="support-col-bad"></div></div>
  <div class="support-col">USB access<div class="support-col-good"></div></div>
</div>

SOC: Snapdragon Wear 2100 (apq8009 for catfish and catfish-ext, msm8909 for catshark)
Storage: 4GB
Port status: Near fully working*
Kernel: Android

# Description
The catfish series are all fairly large round watches with composite cases and two non-rotating buttons. Along with their interesting secondary FSTN LCD used for timekeeping when the OLED display is off (or even when the whole watch is shut down!) they have a very complete set of features. They all come with heartrate, GPS, NFC, step counting and a speaker (useful for making phone calls) and catshark even comes with cellular connectivity which should enable complete independence from a phone. While catfish and catfish-ext get very respectable battery life of up to 3 days, catshark seems to have serious battery issues thanks to the modem and will generally barely last a day. All catfish take standard 22mm straps.
## Variants
TODO: add a list of variants and describe the differences.
- Catshark (Ticwatch Pro 4G/LTE) comes with cellular connectivity. While this gives it complete smarphone independence, it significantly impacts the battery life, lasting just under a day. It is only available in black. The bezel is numbered with 5 minute markers (05-60) and the surface is knurled, similar to the power key. The standard strap is silicone.

# LCD and nanohub
The FSTN LCD on catfish has a number of interesting segments - These seem to be as follows:
- 4 7-segment digits and a colon used to indicated time in minutes and hours
- 5 9-segment digits used to indicate the month and day of month
- 5 rectangular segments (the leftmost shaped like a battery) used to indicate the charge level
- pm indicator
- some segments for step counting (number unknown) + a shoe symbol
- some segments for heartrate (likely 3) + a heart symbol
The LCD is controlled by a dedicated microcontroller called nanohub, which can continue running when the system is completely shut down. Apart from the LCD it is also hooked up to nearly every sensor on the watch, which allows it to keep track of steps and heartrate independently.
The system communicates with the nanohub through a binary blob that sends data to a really ugly interface in sysfs. On narwhal this is done entirely through sysfs commands (which is a far better implementation). Nanohub gets pretty nuts, looking at the data in firmware files suggests that it may even be running a neural network to analyse the data coming in from the sensors, and it seems to expose this for the purposes of sleep and exercise tracking while the watch is off.

## sysfs interface
DO NOT TOUCH THE SYSFS INTERFACE OF CATFISH UNLESS YOU KNOW WHAT YOU ARE DOING. TALK TO SOMEONE KNOWLEDGEABLE FIRST. CATFISH HAVE HAD NANOHUB BRICKED IN THE PAST, LEAVING THE LCD AND SENSORS UNRESPONSIVE. BELOW IS SOME INFORMATION, BUT THIS IS NOT ADEQUATE TO START MESSING WITH SYSFS. YOU HAVE BEEN WARNED.

/sys/class/nanohub/nanohub provides a number of interfaces for communicating. The issue is that it is not known what happens on the other side of this equation, we have firmware files for nanohub but analysing the logic on there is not a project anyone has embarked on.
```
root@catfish:/home/ceres# ls /sys/class/nanohub/nanohub/
app_info            download_bl_status  erase_shared_bl     lock                sensorhal_alive     wakeup
dev                 download_kernel     firmware_version    mode                subsystem
download_app        download_kernel_bl  iio                 power               uevent
download_bl         erase_shared        lcd_mutex           reset               unlock

```
- Don't touch the `lock` file, this will brick your nanohub. A catshark has been restored from this state by restoring to WearOS, but this may be unrecoverable in certain situations. It seems to lock the 'bootloader' of the microcontroller. `unlock` might have something to do with this, but these things are a bit of a black box.
- `reset` restarts the microcontroller.
- anything to do with `download` is to do with flashing firmware to the device. `download...status` files give the status of the firmware upload.

# Repair
All catfish are held together from the back with 4 torx t4 screws and are sealed with a rubber O-ring (no glue to negotiate, water resistance is not compromised after opening). Parts do not seem to be generally available.

# Miscellaneous hardware docs
## Keys
The upper key is the power key.
## Manually getting to fastboot
Power down the watch. Keep holding both buttons during the boot process until the fastboot menu appears.

