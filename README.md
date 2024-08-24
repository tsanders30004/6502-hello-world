# 6502 'HELLO WORLD 6502' PCB

## INTRODUCTION
- The repo has all of the files necessary to build Ben Eater's HELLO WORLD 8-bit computer on a PCB.
- When I started my 6502 learning journey two years ago, it was so I could learn more about 6502 assembly language.
- I had little interest in hardware at the time.
- While I was doing my research, I stumbled on Ben Eater's '8-bit computer on a breadboard' YouTube series and decided to build my own computer.
- I quickly grew frustrated with breadboards so I decided to build a PCB instead.
- After many YouTube vidoes and a failed prototype, I was able to get a working PCB.
- The files in this repo are the result.

## EDA SOFTWARE
The schematics and PCB were designed with KiCad version 6.

## SCHEMATICS
- KiCad and PDF schematics are included.

### Bus vs. Labels

- When I drew the schematics, I could not figure out how to draw a bus.
- Instead, I used lables for the address and data pins, and a few other things.

## INPUTS
### Power
+5 and GND are connected to the circuit via the header pins in the upper-right corner of the PCB.

The PWR LED will illuminate when the PCB has power.

### Clock
You will need an external clock.

The clock signal should be connected to the CLK input pin in the upper-right corner of the PCB.

The CLK LED will illuminate when the circuit has a clock signal.

## OUTPUTS 
### Address and Data Pins
Output pins for each of the data and address lines are arranged vertically along the right side of the PCB.

You can connect these pins to an Arduino, oscilloscope, logic analyzer, etc. if you wish.

Leave them unconnected if you don't want to use them.

### LED's
There are LED's for each of the address and data lines along the bottom.  The LED's will illuminate when a program is running.

## IRQB and RESETB
Note the IRQB and RESETB switches directly above the 65C02 socket. 

When I drew the schematic, I was not certain how to wire the IRQB and RESETB signals using a button.  So I decided to use a slider switch instead; that way, I could connect/disconnect these signals however I wanted.

###  Resetting the Circuit
IMPORTANT:  To reset the cicuit, do the following:

1. Put the IRQB and RESETB slider switches in the UP position.
1. Put the IRQB slider switch in the DOWN position.
1. Put the RESETB slider switch in the DOWN position.

## FILES
|Filename|Description|
|-|-|
|6502_hello_world.kicad_pro|KiCad Project File|
|6502_hello_world.kicad_sch|KiCad Schematic File|
|6502_hello_world.kicad_pcb|KiCad PCB File|
|gerber_files.zip|Gerber Files|
|hello.s|Hello World Source Code|
|hello.out|Hello World Binary File|
|pcb_3d_model.png|Screen Shot of 3D Model|
|schematic.pdf|Schematics|

## CLOSING COMMENTS
- I am a hobbyist.  This is my first attempt at designing a PCB.
- When I started this project, I knew the basics of digital hardware.  But I knew nothing about PCB design.
- I learned how to solder and how to use KiCad via YouTube videos.
- PBCWay used the included gerber files to build the PCB.  They are probably suitable for other PCB manufacturers.
- If not, you can export you own gerber files with KiCad.
