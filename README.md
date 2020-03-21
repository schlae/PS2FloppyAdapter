# PS/2 Floppy Adapter

This PS/2 floppy adapter is designed to allow standard PC floppy drives to be
used in IBM PS/2 systems that have 40-pin edge connectors for their floppy
drive interfaces. Compatible models include

* IBM PS/2 Model 50 and 50Z
* IBM PS/2 Model 60
* IBM PS/2 Model 70
* IBM PS/2 Model 80

And others as well.

The design files are here.

[Schematic](https://github.com/schlae/PS2FloppyAdapter/blob/master/PS2FloppyAdapter.pdf)

[Fab Files](https://github.com/schlae/PS2FloppyAdapter/blob/master/cam/PS2FloppyAdapterRevA.zip)

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
