Tetra (Sony Smartwatch 3) is a rectangular watch with a transflective LCD display and sports-oriented features. Unfortunatley, it suffers from graphical glitches due to the unique Broadcom CPU.
Warning: The Sony Smartwatch 3 is the only watch supported by AsteroidOS using a Broadcom SoC. Its support is known for being experimental. It presents various limitations for a daily usage but is enough to get an overall overview of AsteroidOS.

<div class="support-row">
  <div class="support-col">Display<div class="support-col-good"></div></div>
  <div class="support-col">Touch<div class="support-col-good"></div></div>
  <div class="support-col">Microphone<div class="support-col-bad"></div></div>
  <div class="support-col">Bluetooth<div class="support-col-good"></div></div>
  <div class="support-col">Compass<div class="support-col-good"></div></div>
  <div class="support-col">Haptics<div class="support-col-good"></div></div>
  <div class="support-col">USB<div class="support-col-good"></div></div>
  <div class="support-col">WLAN<div class="support-col-good"></div></div>
  <div class="support-col">Tilt-to-Wake<div class="support-col-good"></div></div>
  <div class="support-col">Always-on-Display<div class="support-col-good"></div></div>
</div>

SOC: Broadcom BCM23550
Storage: 4GB
Port status: Experimental
Kernel: Android

# Description
Tetra is a rectangular watch with a lot of sensors including GPS and NFC. The display is a transflective LCD, which is readable in nearly all lighting conditions and can stay on to provide a very power-efficient always-on display. Uniquely, it charges through an integrated USB micro-B connector (covered by a rubber flap), so there is no dock. The smartwatch 'module' sits inside of a combined strap/frame assembly - straps are available in silicone and metal bracelet styles, and you can even 3D print a replacement case.

## Issues
Tetra suffers from graphical glitches due to the unique Broadcom SoC - the graphics subsystem on this watch is different from the more common Qualcomm watches supported by AsteroidOS, so they are difficult to diagnose and fix. This makes the

# Repair
Opening does not compromise any glue seal so should not compromise water resistance. To open the watch, remove it from the strap, then undo the four screws around the display and pry up on the back metal casing. The display should come off in its frame - beware of the flex cable connecting it to the motherboard. Parts are not generally available. You will likely need to replace the battery when buying these watches as they are getting quite old.

# Miscellaneous hardware docs
## Manually getting to fastboot
[unknown]
