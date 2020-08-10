# BDDrive_MotorController
Modifications done on the open source ODrive project to support one low current brushless DC motor

## Introduction
This project is based on a open source porjet named [ODrive](https://odriverobotics.com/). ODrive is a high power brushless DC motor controller. The main goal of the BDDrive is to modify the ODrive v3.4 to accomodate special needs for a tension controlled braided carrier of composites master's project. In short, there are two main reasons why the BDDrive was conceive. 

Firstly, the most recent ODrive someone can buy is the version v3.6, which was the board used first for testing if this board could be useful for the carrier. Almost everything about the ODrive is open source. The firmware is totally available for free [at this repository](https://github.com/madcowswe/ODrive). Most of the hardware is available, except for the most recent versions v3.5 and v3.6. The creator of the project started to see people copying the project and selling it at a lower price, so he decided to stop to make available the hardware design of the newer versions.Since the most recent board which is on the [hardware github repository](https://github.com/madcowswe/ODriveHardware) is the ODrive v3.4, and this board has many issues, well, it needed to be modified on the BDDrive.

Secondly, ODrive is a **high power** motor controller, it can control motors up to high current (something like 60 Amps, maybe even more). But the carrier is not using high power motors, the highest it goes is around 5 Amps. Since the ODrive is designed for higher current motors, it isn't the best for controlling motor like the tension controlled braided carrier is using. So we needed to fix this on the BDDrive. 

## Repository layout
Here is how the repository is organized and what folder contains what:
- Documentation: contains general documentation for the board
  - Ressources: contains various useful diagrams
  - Requirements: contains files where the requierements of the board are explained, what was modified and for what reason
  - Shunt test: contains screen shots of a test done using a ODrive v3.6 with new shunt resistors designed for low power DC brushless motors
- Hardware: contains the Altium Designer files for the BDDrive embedded circuit (electrical schematics)
  - CAD: contains .step files for electrical integrated circuits (IC) and also a .step file for the whole BDDrive board
  - BOM: contains the bill of materials for the board
  - gerbers: contains files generated with Altium Designer to produce the circuit with the JLC PCB or PCB Way company
  - Altium_libs: contains custom libraries for various electrical parts in the PCB (printed circuit board)
  - v3.4_nbd: contains the schematics and the PCB files for the BDDrive
  - v3: contains the schematics for the ODrive v3.4 board
