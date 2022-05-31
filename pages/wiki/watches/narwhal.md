Narwhal (LG Watch W7) is a watch infamous for having a pair of analogue hands between the display and multitouch glass. The port is nearly complete, but work is still needed to get the hands fully integrated with the system.

<div class="support-row">
  <div class="support-col">Display<div class="support-col-good"></div></div>
  <div class="support-col">Touch<div class="support-col-good"></div></div>
  <div class="support-col">Microphone<div class="support-col-bad"></div></div>
  <div class="support-col">Bluetooth<div class="support-col-good"></div></div>
  <div class="support-col">Haptics<div class="support-col-good"></div></div>
  <div class="support-col">USB<div class="support-col-good"></div></div>
  <div class="support-col">WLAN<div class="support-col-good"></div></div>
  <div class="support-col">Tilt-to-Wake<div class="support-col-good"></div></div>
  <div class="support-col">Hands<div class="support-col-bad"></div></div>
  <div class="support-col">USB access<div class="support-col-good"></div></div>
</div>

SOC: Snapdragon Wear 2100 (apq8009)
Storage: 4GB
Port status: Near fully working*
Kernel: Android

# Description
Narwhal is a fairly large round steel-cased watch with a rotating crown and an additional pair of buttons. The display is quite small compared to the case size and is inset far into the body. The only sensors are a compass and step counter.
The hands come through a hole in the middle of the display, which results in a dead spot of about 2.5mm at the center of the screen, and the hands are always in the way of something. AsteroidOS will eventually try to fix this by moving them out of the way for every item on screen.
Despite the fact that this watch does not need to make use of always on display to show the time, it seems to suffer from really bad battery life, with luckier users getting barely an entire day. This issue comes from the tiny 240 mAh battery. The display is an LCD, so using always on display will increase power draw significantly.
Narwhal takes standard 22mm straps. They are probably worth replacing as the stock straps looks like a bit of an afterthought compared to the rest of the watch.

# Hands
The defining feature of this watch is the pair of hands placed between the LCD and the touch sensitive glass. They are somewhat independent from the watch and will continue to tell the time without the system being booted (advertised battery life of this mode is up to 100 days). They may occasionally become misaligned with the display and will then require calibration.
The hands can be set to a certain position by the system, which they will hold until they recieve another command. The hands can also be set to 'watch mode', which will make them tell the time independently from the watch. If the watch shuts down due to low battery, the hands will continue to tell the time for more than a week. They will eventually also shut down in order to prevent overdischarging of the battery.
The qml module org.asteroid.controls provides the item PhysicalHands which allows easy control of the hands from QML applications.

# Repair
Opening the watch requires the glue seal to be broken, compromising water resistance. The battery seems to be available as BL-S10. When opening the watch, beware the delicate hands mechanism, and make sure that no dust is trapped below the glass after you are done as this is very frustrating. Thankfully, replacing the battery only requires the motherboard to be removed and not the entire frame.

# Miscellaneous hardware docs
## Keys
The central key, being also the rotating crown, is the power key. The top and bottom extra keys map to volume up and down respectively.
## Manually getting to fastboot
Hold either extra key and then the power key to power on the device, hold them until you see the fastboot prompt.
