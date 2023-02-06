# smol-jvs-io

Smol JVS IO is a scoped down JVS I/O board designed to work as a drop-in replacement for arcade stick PCB's, to allow them to interface with JVS hardware. It is not meant to function as a fully functional JVS IO in terms of functionality.

This hardware and software of this board was forked from [td-io](https://github.com/tdaede/td-io) and then heavily scoped down to fit my needs. The td-io firmware is not directly compatible, due to design shortcuts on this board such as removing the shift registers.

At this point, I suppose not much of the td-io hardware schematic is used here any more. The firmware is still a pretty close fork though.

# Features

* JVS IO board interface as one-player device.
* Brook board compatible 20pin connector for hooking up player 1 stick and buttons.
* Upgradeable firmware

# BOM

Note that earlier versions may miss some of these, or have other component identifiers, but overall should be the same.

- U1 ADM3485EARZ-REEL7 or ST3485EBDR (or some other pin compatible one)
- U2 Raspberry Pi Pico
- Q1 AO3400A (Or any similar mosfet)
- D1 BAV99S,115 
- R1 0805 120ohm
- R2 0805 1k ohm
- J1 USBR-B-S-F-O-TH (Digikey: SAM10873-ND)
- J2 JST PH 1x4
- J3 JST PH 1x4
- J4 2.54mm Pinheader 2x10
- J5 JST XH 1x2

# Stuff intentionally not provided

* Player 2 controls
* Chaining other JVS IO boards
* Video/Audio handling
* Analog controls, Mahjong controls...

# Power

Power can either be provided to the micro USB port of the raspberry pi pico, or through the +5V/GND pins of the board.

# Firmware Updates

Flash the Raspberry Pi Pico with new firmware. Make sure stick is not powered from other sources.

# License

CERN-OHL-W
