Sawfish (Huawei Watch 2) and sawshark (Huawei Watch 2 4G/LTE) are a series of round sports-styled watches with a lot of features.
Warning: This watch is often confused with the Huawei watch GT series. These are not capable of running a full version of linux and so will likely never run AsteroidOS.

<div class="support-row">
  <div class="support-col">Display<div class="support-col-good"></div></div>
  <div class="support-col">Touch<div class="support-col-good"></div></div>
  <div class="support-col">Microphone<div class="support-col-bad"></div></div>
  <div class="support-col">Speaker<div class="support-col-bad"></div></div>
  <div class="support-col">Bluetooth<div class="support-col-good"></div></div>
  <div class="support-col">Haptics<div class="support-col-good"></div></div>
  <div class="support-col">USB<div class="support-col-bad"></div></div>
  <div class="support-col">WLAN<div class="support-col-good"></div></div>
  <div class="support-col">Heart Rate<div class="support-col-good"></div></div>
  <div class="support-col">Tilt-to-Wake<div class="support-col-good"></div></div>
  <div class="support-col">USB access<div class="support-col-good"></div></div>
</div>

SOC: Snapdragon Wear 2100 (apq8009 for sawfish, msm8909 for sawshark)
Storage: 4GB
Port status: Near fully working*
Kernel: Android

# Description
Sawfish is a rather compact plastic watch with 2 buttons and an oled display. They have most of the features you might want - GPS, compass, NFC, a speaker, step counter and heartrate sensor.

## Variants
- Huawei Watch 2 is the standard version. It comes with a plastic case (which is known for shattering around the lugs, making the watch unwearable), but this doesn't affect many watches. It takes 20mm straps, and comes with integrated straps preinstalled though these can be replaced.
- Huawei Watch 2 4G/LTE (sawshark) is just like the standard version but comes with LTE. It suffers from the same fragility issue. Removing the back cover will reveal a sim card slot.
- Huawei Watch 2 2018 is the china version of the 4G/LTE. It replaces the sim card slot with an esim.
- Huawei Watch 2 Classic is a sawfish (no LTE) that comes in a metal case with 22mm straps. This does not suffer from the issue of fragile lugs. There is no metal version of sawshark due to issues with the permeation of a 4G signal. It should be possible to swap sawshark internals into a sawfish body, but it is not known how severely this affects the connection.

# Repair
All sawfish are held together from the back with 4 torx t2 screws and are sealed with a rubber O-ring (no glue to negotiate, water resistance is not compromised after opening). Parts show up from time to time, and there are many watches out there for parts with broken lugs.

# Miscellaneous hardware docs
## Keys
The upper key is the power key.
## Manually getting to fastboot
Press and hold the power button when the manufacturer bootlogo appears, until the vibration finishes. Release the button and press it again quickly. The time frame for this method is short and might need several attempts. Some users report that repeated power button presses already during the vibration helps.

