Ray and Firefish are based on the Fossil Gen 4 platform and are available under several names and brands. Models were released by Fossil, Skagen, Diesel, Michael Kors (and possibly others).

<div class="support-row">
  <div class="support-col">Display<div class="support-col-good"></div></div>
  <div class="support-col">Touch<div class="support-col-good"></div></div>
  <div class="support-col">Microphone<div class="support-col-bad"></div></div>
  <div class="support-col">Bluetooth<div class="support-col-good"></div></div>
  <div class="support-col">Haptics<div class="support-col-good"></div></div>
  <div class="support-col">USB<div class="support-col-good"></div></div>
  <div class="support-col">WLAN<div class="support-col-good"></div></div>
  <div class="support-col">Heart Rate<div class="support-col-good"></div></div>
  <div class="support-col">Tilt-to-Wake<div class="support-col-good"></div></div>
  <div class="support-col">USB<div class="support-col-bad"></div></div>
</div>

SOC: Snapdragon Wear 2100 (apq8009)
Storage: 4GB
Port status: Fully working
Kernel: Android

# Description
The difference between the two models is the display size - otherwise the two images are completely interchangeable, and work fine but with a badly sized display. The watches have a rotating crown with 2 additional buttons, and come with a stepcounter and both GPS and heartrate monitoring, which are both nice to have for sports purposes - unfortunately the GPS is rather power hungry and limits battery life to less than a day. The watches are also, frustratingly, missing a compass, which makes GPS navigation a bit less user-friendly.

# Getting USB
## Available docks
If you are fine with not having USB access most of the time, you can 3d print a dock that will dock to the watch when the back cover is removed.

### Read before reassembly
Before securing the watch, make sure to connect your watch to a wifi network using connmanctl. Otheriwise, you won't have shell access which will lock you out of a lot of features.
When reassembling the watch, make sure not to use adhesive that is very strong. You will eventually need physical SSH access when something inevitably breaks - at this point you will need to pull the back off again and use the dock.
## Replacement backplates
A more permanent but more complicated solution is the replacement backplate. These will expose USB permanently so that you can access it whenever you want without opening the watch. All the following designs are 3d printed.
### Hotdog design
This design, courtesy of hotdog18882, makes use of a fairly common magnetic connector that is commonly available on aliexpress. The main disadvantage is that you lose the heartrate sensor. However, the design is easy to print on any 3d printer and the cables are very common and so you can buy several chargers for very cheap.
Assembly instructions:
### Dodoradio design
This design, courtesy of dodoradio, makes use of two sets of pogo pins and is completely solderless. This probably cannot be printed on an FDM 3d printer as it takes advantage of tight geometry and clarity. This design attempts to keep the functionality of the heartrate sensor, some tuning might be needed to get that working however.
Assembly instructions

## Location on the board
USB is not available on these watches by default. It is exposed in two places once you remove the back casing of the watch.
TODO: add images of the contact pads on the watch
The outer charging rings are 5v (inner,1) and ground (outer,2). These are picked up on the motherboard with a pair of spring contacts, 5v (3) and ground (4). A set of 4 pads is present around the connector for the heartrate flex (5). On the left, the bottom pad is 5v (6) and the top pad is ground (7), these directly duplicate the charging rings. The data pads are on the right of the connector. The top pad is data+ (8) and the bottom pad is data- (9). These are also directly duplicated on the heartrate flex cable, and can be accessed by removing a sticker (10) or folding up the extended section. The ring closest to the center is d+ (11) and the outer one is d- (12).

# Visual description
