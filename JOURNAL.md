# SplitKeeb Journey

## Day 1: Planning

Im officially committing to a build.

The plan is a split keyboard built around XIAO-nRF52840 controllers (for 2 sides
as in split keyboard guided project) a 5-column, 6-row layout (so 5x6 x2). I
want it to feel modern, so I’m going for addressable RGB, hotswappable MX
sockets, and Gateron 3.0 Red switches. Firmware-wise, I’m choosing ZMK.

So the Materials needed might turn into something like

- 2x XIAO-nRF52840
- 10 x 1.25A Blank Keycaps
- 50 x 1A Blank Keycaps
- (60 ± 2) x Gateron G Pro 3.0 (Red or Brown) Switches
- (60 ± 2) x Diodes (gotta choose one am not sure to use SMD or through-hole(THT
  ig))
- 4 x M3x16mm screws
- 4 x M3x5mx4mm heatset inserts
- 3d printed case (obviously)

Idk if i buy things ± 2 or more. as this is my second project i will probably
make so many mistakes. The above list is subjected to change as i don't know
what i will add/remove.

I initially wanted to design a fully custom PCB from scratch using the RP2040.
In my head it sounded like a “proper build.” But in reality, it’s not in my
league right now. I’m not trying to turn this into a failure.

So the new goal is to build something I can actually finish.

A keyboard that works first, and then gets refined.

Still, it feels like the good starting point. I’m not building the perfect
keyboard. I’m building my first real SplitKeeb. And its my second project using
PCB's and 3D printed case (last was obviously the hackpad) Also this is my first
time writing a journal so... The Journals might have some issues with usage of
English and other stuff.

And i tried to figureout a simple schema for the board ![schema1](schema1.png)
![schema2](schema2.png)

## Day 2: Planning again

Time: 9am - 11am I think my Day 1 plans are not enough Idk am overwhelmed with
the possibilities I need to figure out another micro controller to achieve a
better keyboard that I can Daily Drive.\
Controller will be Based on RP2040 probably Maybe i will build a custom micro
controller (dev board) using the
[Hackclub Tutorial](https://blueprint.hackclub.com/starter-projects/devboard)
and my own magic ig

Time: 1pm - 5pm At last i figured out that i will use RP2040-Zero
[Wiki](https://www.waveshare.com/wiki/RP2040-Zero)
[Datasheet](https://m.media-amazon.com/images/I/A1tLPy1hLqL.pdf)

And the keyboard layout will be
![r1](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MjUyNTksInB1ciI6ImJsb2JfaWQifX0=--6a67ed215970b40d58aad122961d0cb56b743b8a/r1.png)

First i thought of using the TRRS Connection between the keyboards. Then i
realized that i can use USB C for the interconnection to use so that i can use
USB C to USB C cables.

PCB design is in progress and i expect it to finish by tomorrow.

Also for the case i will be checking out If i can use the PCB Layering (idk what
its called gotta check that) and the possibilities to build 2 pcb on top and
bottom of it

Time 6pm - 10:30pm Starting on PCB design. Finding out How i can interconnect
both sides via USB-C Spend a lot of time searching for USB-C and how to do the
schematics

The schematics will be
![keyboard-layout](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MjUyNjIsInB1ciI6ImJsb2JfaWQifX0=--c8eef0d7afacd67a3fdbecb6667f6d38e6a8dec4/keyboard-layout.png)
![l2](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MjUyNjEsInB1ciI6ImJsb2JfaWQifX0=--c34825d12b2facfc1777f1c6e861d1d756d01b3f/l2.png)
![r2](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MjUyNjAsInB1ciI6ImJsb2JfaWQifX0=--a17be29a074677bb96912c7d92d9379ca3912d07/r2.png)
![l1](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MjUyNTgsInB1ciI6ImJsb2JfaWQifX0=--a444f73a205c3f248927b9e99bb547e36c733037/l1.png)

Found some useful articles and projects for inspiration
[ErgoDonk Zero](https://github.com/JellyTitan/ErgoDonk-Zero)
[Hardware design with RP2040](https://pip-assets.raspberrypi.com/categories/814-rp2040/documents/RP-008279-DS-1-hardware-design-with-rp2040.pdf)

Custom DIY Keyboard Design and Build: Schematic + PCB + Case | Part 1 - RP2040
by Robert Feranec: [Video](https://www.youtube.com/watch?v=N4cLFE0FF2U) |
[OSHWLab Link](https://oshwlab.com/robertferanec/custom-keyboard)

[How to Design Mechanical Keyboard PCBs with Kicad by Joe Scotto](https://www.youtube.com/watch?v=8WXpGTIbxlQ)

[How To: Split Keyboard with RP2040 and KMK](https://sanderg.nl/en/posts/how-to-split-keyboard-with-rp2040-and-kmk/)

## Day 3: Starting to work on PCB

#### KB Placer or No KB Placer ?

##### Time: 7-8:15am

I tried to use KB Placer to place my layout with my keyboard-layout.json by
[keyboard-layout-editor](https://www.keyboard-layout-editor.com/) But searching
through slack i found that some one got banned for using
[EroGen](https://github.com/adamws/kicad-kbplacer) and
[KB Placer](https://github.com/adamws/kicad-kbplacer), I don't need that fate to
my split keyboard. So am still waiting for the Slack Support to get me a Answer
to use or not use the plugin (i need it soooo bad to place the keys for my
keyboard, no routing or other fancy stuff)

[kbplacer image]

##### Time: 8:15am - 10:15am

I think i will do it without the KBPlacer ig, but it will take so much time than
using that. soooooo i need someone to help me to decide to use or not use
KBPlacer plugin for the layout.

Anyways am starting to do the PCB Layout by hand rn. to spend my time
efficiently

I started the pcb design and found out that the RP2040 symbols and footprints
where invalid when i referred the
[RP2040-Zero Wiki](https://www.waveshare.com/wiki/RP2040-Zero)

Then i found that i should use SK6812MINI-E Instead of SK6812MINI. Spend working
till 8pm. Now i hopefully found the repo with the footprints and symbols,
[marbastlib](https://github.com/ebastler/marbastlib) Am redoing the PCB again...

## Day 4: Working on schematics and improving it

I added my schematic for review in `#blueprint` in Hackclub Slack , `@sandgum`
helped me to figure out the logic level converter and some resistors i should
use

The pcb structure is ready. Added 0.1uF(100nF) Capacitors to the

## Day 5: Final schematics and pcb for left side.

I didn't time my things as am lazy, But the changes made are use 0.1uF
capacitors as recommended in the sk6812mini-e docs.

Added A ESD protection circuit inspired from YAMEK keyboards, fixed the
schematics and wireup the pcb the result looks like

## Day 6: ReImplementation ??

Updated the schematics to use a much better MCU, add a Battery, 2.4ghz
(interconnection and connection with a dongle if possible), BLE and a overall
better schematics.

I will hopefully finish the pcb by 2 days, i will start working on the 3d model
for the case tommorrow.

![screenshot_2025-12-21_23-53-51](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MjcyNzgsInB1ciI6ImJsb2JfaWQifX0=--1b2ac715ef4c69fddaaacf9c8db1641ad04fe6ef/screenshot_2025-12-21_23-53-51.png)
![screenshot_2025-12-21_23-53-12](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MjcyNzcsInB1ciI6ImJsb2JfaWQifX0=--1abe404f2f1675f54cd9f09846fa97274a9c595a/screenshot_2025-12-21_23-53-12.png)
![screenshot_2025-12-21_23-53-40](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MjcyNzYsInB1ciI6ImJsb2JfaWQifX0=--7b3c3b924143769346b0b7305e70dd898d02d445/screenshot_2025-12-21_23-53-40.png)
![screenshot_2025-12-21_23-53-26](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MjcyNzksInB1ciI6ImJsb2JfaWQifX0=--7892d6466546c55bb0d7998660e3efcbb51e5d97/screenshot_2025-12-21_23-53-26.png)

# Reference Links

## Display

- **Nice!View**\
  https://shop.beekeeb.com/products/nice-view-with-sockets-power-saving-display-for-wireless-split-keyboard

## MCU / Wireless

- **Holyiot 18010 module**\
  Datasheet: http://www.holyiot.com/tp/2019042516322180424.pdf\
  Robu.in: https://robu.in/product/holyiot-18010-nrf52840-chipset-ble-module/

## Switch Sockets

- **Gateron Hot-swap PCB Socket 2.0 (KS-2P02B01-01)**\
  Datasheet:
  https://gateron.com/u_file/2311/22/file/GATERONUpgradeHot-swapPCB20Socket-KS-2P02B01-01-a.pdf

## LEDs

- **SK6812MINI-E (addressable RGB LED)**\
  Datasheet:
  https://cdn-shop.adafruit.com/product-files/4960/4960_SK6812MINI-E_REV02_EN.pdf

## USB-C

- **USB Type-C receptacle (HRO TYPE-C-31-M-23, right-angle, 16P, SMD)**\
  Product page:
  https://robu.in/product/type-c-31-m-23-hroparts-1-surface-mount-right-angle-16p-female-55%e2%84%8385%e2%84%83-type-c-smd-usb-connectors-rohs/

## Debug / Tools

- **Raspberry Pi Debug Probe**\
  Documentation:
  https://www.raspberrypi.com/documentation/microcontrollers/debug-probe.html

## Logic / Level Shifting

- **SN74LV1T125DBV (single-channel level translator / buffer)**\
  Digi-Key:
  https://www.digikey.in/en/products/detail/texas-instruments/SN74LV1T125DBVR/4555571\
  Datasheet: https://www.ti.com/lit/ds/symlink/sn74lv1t125.pdf

## Battery Charging (idk i will probably change it soon)

- **BQ24090DGQ (Li-ion charger / power path)**\
  Digi-Key:
  https://www.digikey.in/en/products/detail/texas-instruments/BQ24090DGQT/2237296\
  Datasheet _(BQ24092 family doc)_:
  https://www.ti.com/lit/ds/symlink/bq24092.pdf

## Connectors

- **JST 2P 2.0mm**\
  AliExpress: https://www.aliexpress.com/item/1005006034725605.html

## ESD Protection

- **USBLC6-2SC6**\
  Digi-Key:
  https://www.digikey.in/en/products/detail/stmicroelectronics/USBLC6-2SC6/1040559\
  Datasheet: https://www.st.com/resource/en/datasheet/cd00050750.pdf

## Voltage Regulators

- **XC6206P332MR (3.3V LDO regulator)**\
  Digi-Key: https://www.digikey.in/en/products/detail/umw/XC6206P332MR/17635277\
  LCSC: https://www.lcsc.com/product-detail/C5252899.html
