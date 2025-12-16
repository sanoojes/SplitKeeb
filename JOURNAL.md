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
