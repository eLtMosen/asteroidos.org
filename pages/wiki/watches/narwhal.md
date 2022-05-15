Narwhal (LG Watch W7) is a watch infamous for having a pair of hands pass through the display.

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
  <div class="support-col">USB<div class="support-col-good"></div></div>
</div>

SOC: Snapdragon Wear 2100 (apq8009)
Storage: 4GB
Port status: Near fully working*
Kernel: Android

# Description
The LG Watch W7 is a fairly large steel-cased watch with a rotating crown and an additional pair of buttons. The display is quite small compared to the case size and is inset far into the body. There only sensors are a compass and step counter. The hands come through a hole in the middle of the display. This results in a dead spot of about 2.5mm at the center of the screen, and the hands are always in the way of something. AsteroidOS will eventually try to fix this by moving them out of the way for every item on screen.

# Hands
The defining feature of this watch is the pair of hands placed between the LCD and the touch sensitive glass. They are somewhat independent from the watch and will continue to tell the time without the system being booted (advertised battery life of this mode is up to 100 days). They may occasionally become misaligned with the display and will then require calibration.
The hands can be set to a certain position by the system, which they will hold until they recieve another command. The hands can also be set to 'watch mode', which will make them tell the time independently from the watch. If the watch shuts down due to low battery, the hands will continue to tell the time for more than a week. They will eventually also shut down in order to prevent overdischarging of the battery.
The qml module org.asteroid.controls provides the item PhysicalHands which allows easy control of the hands from QML applications.



