# E-Z Field Fone

This repository contains a project for an intercom / field phone. The design uses discrete components throughout.  

The design includes:
- KiCad 10 Schematic and PCB files
- KiCad 10 SPICE Simulation Workbook
- Gerber files for fabrication  
- PDF schematic export and PCB screenshots for easy viewing without KiCad

# How It Works

The audio input (from on-board mic, or via a handset/earpiece jack socket) is amplified, then sent over bell wire to the remote unit. The signal on the bell wire is fed into a difference amplifier, in order to subtract the local audio. The difference output is fed into a power amplifier. The user can signal a call alert by applying a DC voltage onto the bell wire. There is an amplifier that is sensitive to DC, and the output can be used to light an indicator or sound a buzzer alert.

![K1 Schematic](block-diag.png)

# Printed Circuit Board Overview

The design is split up into two separate printed circuit boards (PCBs). One PCB contains the microphone amplifier (Mic Booard) and the other contains everything else (Main Board). You'll need a mic board, and a main board, for each unit. The two boards are designed to fit into at least a couple of different enclosures. 
