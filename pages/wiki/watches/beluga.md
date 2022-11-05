Beluga (OPPO Watch) is a large rectangular watch that is currently in experimental support. It features a modern looking display with a large amount of sensors. It suffers from graphical glitches due to incompatible GPU libraries.

Warning: The OPPO Watch Free is not supported! See the list on the <a href="{{rel 'wiki/porting-status'}}">porting status</a> page to find out if your model is supported.

<div class="support-row">
  <div class="support-col">Display<div class="support-col-good"></div></div>
  <div class="support-col">Touch<div class="support-col-good"></div></div>
  <div class="support-col">Microphone<div class="support-col-bad"></div></div>
  <div class="support-col">Speaker<div class="support-col-bad"></div></div>
  <div class="support-col">Bluetooth<div class="support-col-good"></div></div>
  <div class="support-col">GPS<div class="support-col-bad"></div></div>
  <div class="support-col">Compass<div class="support-col-good"></div></div>
  <div class="support-col">Haptics<div class="support-col-good"></div></div>
  <div class="support-col">USB<div class="support-col-good"></div></div>
  <div class="support-col">Heart Rate<div class="support-col-good"></div></div>
  <div class="support-col">WLAN<div class="support-col-bad"></div></div>
  <div class="support-col">Tilt-to-Wake<div class="support-col-good"></div></div>
  <div class="support-col">NFC<div class="support-col-bad"></div></div>
</div>

SOC: Snapdragon 3100 (msm8909w)
Storage: 8GB
Port status: Experimental
Kernel: Android

# Description
Beluga is a large rectangular watch with a (side) curved OLED display, fairly large amount of sensors and a good vibration motor.
The casing of the watch is relatively thin, making it easier to tuck under the sleeves.
The watch uses a proprietary watchband mechanism for which one can buy adapters so standard 22mm straps can be attached.

## Issues
Beluga suffers from graphical glitches due to incompatible GPU drivers originally used for the Wear 2100 platform.

# Repair and customisation
The back of the watch is held on by glue, which means that disassembly will impact water resistance and is somewhat frustrating.

# Miscellaneous hardware docs
## Keys
There are two hardware buttons located on the right of the watch.
The top button can be used to navigate through the 

The bottom button is used to power on or hard reset the watch.
The top button can be used to wake/sleep the watch from AsteroidOS. This button is also used to navigate through the boot menu.


## Manually getting to fastboot
When the watch is unlocked you can easily enter fastboot by pressing the upper right hardware button during the bootup of the watch. This will make the watch enter a boot menu. Using the top button to cycle through the list. Once "Fastboot" is selected press the bottom button to boot to fastboot.
