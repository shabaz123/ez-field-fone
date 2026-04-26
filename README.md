# E-Z Field Fone

This repository contains a project for an intercom / field phone. The design uses discrete components throughout.  

The design includes:
- KiCad 10 Schematic and PCB files
- KiCad 10 SPICE Simulation Workbook
- Gerber files for fabrication  
- PDF schematic export and PCB screenshots for easy viewing without KiCad

# How It Works

The audio input (from on-board mic, or via a handset/earpiece jack socket) is amplified, then sent over bell wire to the remote unit. The signal on the bell wire is fed into a difference amplifier, in order to subtract the local audio. The difference output is fed into a power amplifier. The user can signal a call alert by applying a DC voltage onto the bell wire. There is an amplifier that is sensitive to DC, and the output can be used to light an indicator or sound a buzzer alert.

![Block Diagram](block-diag.png)

# Printed Circuit Board Overview

The design is split up into two separate printed circuit boards (PCBs). One PCB contains the microphone amplifier (Mic Booard) and the other contains everything else (Main Board). You'll need a mic board, and a main board, for each unit. The two boards are designed to fit into at least a couple of different enclosures. 

# Enclosures

The circuit boards will comfortably fit inside a Hammond 1559E enclosure (170 x 85 x 34 mm) along with a large 60 mm diameter (66 x 66 mm square) 8 ohm speaker such as Pui AS06608PS-R and a PP3 battery. 

If you prefer to omit the speaker and use an external handset, then a smaller Hammond 1593X (140 x 66 x 28 mm) can be used. 

If you wish to use any other enclosure, the PCB dimensions are:

Mic Board: 59 x 32.5 mm

Main Board: 59 x 55 mm

# Mic Board

The mic board uses a preamplifier designed by M. Kellett.

- **Gain:** ~45 dB  
- **Bandwidth (-3 dB):** ~100 Hz to 7 kHz (approximate)

## Schematic

![Mic Board Schematic](mic-board/mic-board-schematic.png)

## Board Connections

Two sets of soldered connections need to be made to the Mic Board; the microphone element, and the speaker. Also, an 8-pin connector is used to attach the Mic Board to the Main Board.

### Electret Mic Element

The Mic Board has a 2-pin location for soldering an electret mic element using screened cable

### Speaker

There is a 2-pin location for soldering an 8-ohm speaker

### Interfacing Connector

An 8-pin connector is used to connect a cable between the Mic Board and the Main Board. A ready-made JST PH 8-way "opposite direction" cable can be used (available from AliExpress). The "opposite direction" means that when laid flat, opposite sides of the connector are seen from one end to the other (this means that pin 1 of the both connectors are attached to each other, and pin 2 of both connectors are attached to each other, and so on; in contrast, a "same direction" cable has pin 1 on one connector wired to pin 8 of the other connector, and pin 2 to pin 7, and so on). Double-check you have the correct cable.

## 3.5 mm Audio Jack Pinout

If you wish to plug in an external mic and speaker/eaerphone, use the 3.5 mm 3-pin socket. Connections are:

- Tip: Audio Out, connect this to any earphone or headphones, or to an 8-ohm speaker
- Ring: Microphone, connect this to an electret mic element (the Mic Board PCB supplies a low voltage to power the element)
- Shield: Ground

## PCB Top

![Mic Board Top](mic-board/mic-board-top.png)

## PCB Underside

![Mic Board Top](mic-board/mic-board-underside.png)

## PCB Render

![Mic Board Render](mic-board/mic-board-render.png)

---

# Main Board

The main board includes a 280mW audio amplifier designed by M. Kellett. 

## Schematic

![Main Board Schematic](main-board/main-board-schematic.png)

## PCB Top

![Main Board Top](main-board/main-board-top.png)

## PCB Underside

![Main Board Top](main-board/main-board-underside.png)

## PCB Render

![Main Board Render](main-board/main-board-render.png)

---

## Notes

All components are easy to source. 

For the input power, use a 9V PP3 battery, or use the 9V DC barrel socket (center positive).



For the audio input and output, an AliExpress stereo audio jack socket can be used (only the tip and the screen is used, the ring is not connected). Alternatively, the audio connections can be made with 0.1" pin headers (they will fit in the same footprint, as there are extra holes for that). 

The potentiometer can be ALPS RK097 series (available from AliExpress), it has pins at 2.5 mm pitch, and a body width of 10 mm.






