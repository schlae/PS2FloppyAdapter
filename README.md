# PS/2 Floppy Adapter

This PS/2 floppy adapter is designed to allow standard PC floppy drives to be
used in IBM PS/2 systems that have 40-pin edge connectors for their floppy
drive interfaces. This can be quite useful because many PS/2 floppy drives have failed due to leaking capacitors or mechanical problems, and can be difficult or impossible to repair.

Compatible models include

* IBM PS/2 Model 50 and 50Z
* IBM PS/2 Model 70

![Photo of floppy drive with adapter hardware mounted](https://github.com/schlae/PS2FloppyAdapter/blob/master/images/assembled_floppy_adapter.jpg)

Here's what the adapter looks like when installed in a Model 50Z.

![Photo of floppy drive with adapter installed in a computer](https://github.com/schlae/PS2FloppyAdapter/blob/master/images/floppy_adapter_installed.jpg)

## Connector PC Board

There are several pieces to the design. First, there is a circuit board: the design files are here.

[Schematic](https://github.com/schlae/PS2FloppyAdapter/blob/master/PS2FloppyAdapter.pdf)

[Fab Files](https://github.com/schlae/PS2FloppyAdapter/blob/master/cam/PS2FloppyDaughterboardRevA.zip)

The bill of materials is as follows:

| Designator | Quantity | Description                  |
| ---------  | -------- | ---------------------------- |
|        J2  |        1 | 34-pin 0.1" breakaway header |
|      R1-R5 |        5 | 1K ohm resistors, 0603       |

Note that R1-R5 can be either 1% or 5% since the exact value is not critical.

J3 provides power to the PC floppy drive. One way to build it is to cut off
a 0.1" power header from an old PC power supply, Y splitter, or similar
adapter, and then solder the wires to the appropriate connections on the
adapter board. Black to ground, red to +5V, and yellow to +12V.

You'll also need a short length of 34-pin ribbon cable with a male IDC connector crimped onto each end. This connects the adapter board to the floppy drive.

## Mechanical Parts

Several parts mechanically adapt the standard PC floppy drive to fit in the
PS/2. Each of them can be printed on a commodity FDM 3D printer.

[Drive Sled](https://github.com/schlae/PS2FloppyAdapter/blob/master/mech/PS2_50_floppy_sled_15F7502.STL) - This is compatible with IBM FRU 15F7502. 

[Plugboard](https://github.com/schlae/PS2FloppyAdapter/blob/master/mech/PS2_50_floppy_plugboard.STL) - The plugboard sits between the floppy drive and the connector PC board, holding it at just the right angle.

[Eject button (Sony MPF920)](https://github.com/schlae/PS2FloppyAdapter/blob/master/mech/PS2_50_floppy_button_sony_mpf920.STL) - Eject button for the Sony MPF920 floppy drive

[Eject button (Teac FD235HF)](https://github.com/schlae/PS2FloppyAdapter/blob/master/mech/PS2_50_floppy_button_teac_fd235HF.STL) - Eject button for the Teac FD235HF floppy drive

The STL files are oriented in the optimal orientations for printing. The sled has some overhangs and will require supports to be added in order to print correctly.

* Two M3-0.5mm, 5mm long self tapping screws. These attach the PCB to the plugboard.

* Four M3-0.5mm, 10mm long machine screws. These attach the floppy drive to the sled.

## Assembly

Remove the old floppy drive bezel. The exact way to do this varies depending on the drive, but typically there are plastic tabs on the sides that clip into the drive. On some drives you may have to remove the metal lid to get at them.

Remove the old eject button from the floppy drive. The Sony drive button simply slides up. You might have to rock it back and forth a bit. The Teac drive button is harder to remove; if you get in with a dental pick or screwdriver, pull up the plastic catch and the button should slide straight out.

Install the new eject button just like you removed the old one but in reverse. If it refuses to go in, don't force it. There are some fairly detailed features that may require cleanup with a sharp knife in order for it to fit.

Before installing the drive on the sled, take the sled and heat the plastic locking tab in the front with a hair dryer or heat gun (low heat) and bend it down. It needs to bend down far enough to engage with a slot in the PS/2 chassis which locks it in place when it is installed.

Then, using the 10mm machine screws, install the drive on the sled. The floppy drive slot should face the same direction as the locking tab on the sled.

Install the PC board on the plastic plugboard using the two self-tapping screws. You can temporarily tape it in place to figure out how long the 34-pin IDC cable and the drive power cable need to be.

Now slide the assembly into your PS/2 computer and plug the PC board into the slot at the back of the drive bay. The plugboard should rest on the top of the floppy drive. Make a mark so you know exactly where it should go. Then remove the assembly and glue the plugboard to the top of the floppy drive, right where you placed your mark. You can try using double-sided tape, but 3M VHB (Very High Bond) is probably the most secure.

I've found that the drive LED lines up fairly well with the LED window on the stock PS/2 drive bezel (IBM FRU 15F7534).

![Photo of the assembly installed in the PS/2](https://github.com/schlae/PS2FloppyAdapter/blob/master/images/floppy_adapter_installed2.jpg)

There is a variant of the drive bezel, FRU 62X0362, which has the LED above the drive slot, which won't work. You'll need to run a wire and hot glue the LED on top of the floppy drive or print a replacement bezel (see below).

## Optional Parts

I've also made a 3D-printable model of the PS/2 Model 50/50Z drive bezel if you want to install this drive as a second floppy drive, or if your machine was missing it.

![Photo of the 3D-printed drive bezel installed in the PS/2](https://github.com/schlae/PS2FloppyAdapter/blob/master/images/floppy_adapter_faceplate.jpg)

This part is tricky to print and requires support structures. It is printed on the side so that the front panel texture will look reasonable, and also so that the plastic locking tabs will be sturdy. Use pliers and side cutters to remove the support structure, and be sure to wear safety glasses!

## Archive

Here is the old version of the floppy adapter PC board. This can be used to electrically connect a floppy drive to the IBM 40-pin connector used on some additional models, such as the Model 60 and 80. There is no mechanical mounting design for these models yet.

[Fab Files](https://github.com/schlae/PS2FloppyAdapter/blob/master/cam/PS2FloppyAdapterRevA.zip)


