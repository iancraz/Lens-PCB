# Lens-Maker PCB
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" width="100" src="./docs/by-nc-sa_small.png" /></a><br />


This repository contains the design files for a printed circuit board (PCB) that enables the control of three stepper motors using an A4988 driver and an ESP32-WROOM32E microcontroller module. The PCB provides a compact and convenient solution for incorporating stepper motor control into your projects.

<img src="./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/PCB%203D%20Print/Lens-Maker_ISO.png" width="600" >

# Table of contents

* [Overview](#overview)
* [Features](#features)
* [Repository Structure](#repository-structure)
* [PCB Design](#pcb-design)
* [Bill of Materials (BOM)](#bill-of-materials)
* [Fabrication Instructions](#fabrication-instructions)
* [Contributing](#contributing)
* [License](#license)

## Overview
>[Table of contents](#table-of-contents)

The purpose of this PCB design is to simplify the process of controlling three stepper motors in your projects. By integrating an A4988 driver and an ESP32-WROOM32E module on a single board, you can easily interface with the motors and leverage the features of the ESP32 for advanced control and communication capabilities. In this design in particular three 2(A) stepper motors where needed to be controlled for a lens maker lathe, and the PCB was designed to fit the casing of the lathe.

# Features
>[Table of contents](#table-of-contents)

* **Compact**: The PCB is designed to be as small as possible while still providing the necessary features for stepper motor control.
* **Integrated A4988 Driver**: The A4988 driver is integrated into the PCB, eliminating the need for a separate driver module.
* **Integrated ESP32-WROOM32E Module**: The ESP32-WROOM32E module is integrated into the PCB, eliminating the need for a separate microcontroller module.
* **Integrated WiFi and Bluetooth Antennas**: The ESP32-WROOM32E module includes integrated WiFi and Bluetooth antennas, eliminating the need for external antennas.
* **Integrated Power Supply**: The PCB includes a 5V power supply that can be used to power the ESP32-WROOM32E module and the A4988 driver.
* **Integrated USB to UART Converter**: The PCB includes a USB to UART converter that can be used to program the ESP32-WROOM32E module and communicate with it via serial.
* **Integrated Reset Button**: The PCB includes a reset button that can be used to reset the ESP32-WROOM32E module.
* **I2C, SPI and GPIO Headers**: The PCB includes headers that can be used to connect I2C, SPI and GPIO devices to the ESP32-WROOM32E module.
* **JTAG Header**: The PCB includes a header that can be used to connect a JTAG debugger to the ESP32-WROOM32E module.
* **USB-C Connector**: The PCB includes a USB-C connector that can be used to power the PCB and communicate with the ESP32-WROOM32E module via USB.

# Repository Structure
>[Table of contents](#table-of-contents)

The repository is organized as follows:

* **`Lens-Maker`**: This directory contains the Altium design files for the PCB.
    * **`Project Outputs for Lens-Maker`**: This directory contains the Output files of the project.
        * **`GerberX2`**: This directory contains the Gerber files of the PCB.
        * **`Lens-Maker_Schematic.PDF`**: This file contains the PDF of the PCB.
        * **`ExportSTEP`**: This directory contains the 3D model of the PCB.
        * **`BOM`**: This directory contains the Bill of Materials of the PCB. 
* **`docs`**: This directory contains the documentation images for the PCB.
* **`LICENSE`**: This file contains the license for the PCB design.
* **`README.md`**: This file contains the documentation for the PCB design.

# PCB Design
>[Table of contents](#table-of-contents)

This PCB was design using Altium Designer 23.4.1. The PCB design files can be found in [here](./Lens-Maker). The PCB was designed to be as small as possible while still providing the necessary features for stepper motor control. The PCB is a 6-layer board with the following stackup:

<img src="./docs/stack_up.png" width="1000" >


The PCB was designed to fit the casing of the lens maker lathe, and the dimensions of the PCB are as follows:


<img src="./docs/PCB_dimensions.png" width="800" >

## Microcontroller
>[Design](#design)

The design of this PCB starts at the desition of the MCU chosen for this purpose. Because of its simplicity and WiFi and Bluetooth antennas already integrated, an ESP32-WROOM-32E is chosen for this design. The main advantages of choosing this microcontroller are:

* **The form factor**: Its a MCU with WLAN capabilities in a size of a regular MCU.
* **Antennas integrated**: The benefits of using an ESP32 module and not an ESP32 MCU is to have the antennas already routed an integrated.
* **Easy to use**: Its many integration generated that ESP32 is a widely used MCU around the world, and this means there's a lot of information and resources to program this MCU.
* **Versatility**: If there is a future design, a new ESP32 module can be changed and the software will 'just work'.

## Stepper Driver
>[Design](#design)

For the Stepper driver, since this design is a prototype approach for the final goal, an A4988 driver was chosen, because of its previous use on a concept desing using the A4988 module from arduino. For future progress a driver change is needed to drive more heavy power Stepper motors. However this driver has a lot of advantages, its ease of use and simplicity makes it really easy tu use and code it, and its application in its own module has the heritage needed for the circuit to rely on.

## Schematic
>[Table of contents](#table-of-contents)


The Schematic of this PCB can be found in [here](./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/Lens-Maker_Schematic.PDF). And below are some images sumarizing it. 

<img src="./docs/sch/Lens-Maker_Schematic-01.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-02.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-03.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-04.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-07.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-08.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-09.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-10.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-11.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-13.png" width="1000" >
<img src="./docs/sch/Lens-Maker_Schematic-14.png" width="1000" >


# Bill of Materials
>[Table of contents](#table-of-contents)

| Designator                                                                                         | Footprint       | Value | Manufacturer                         | Manufacturer Part Number | Supplier | Supplier Part Number | Description                                                                                              | Quantity |
| -------------------------------------------------------------------------------------------------- | --------------- | ----- | ------------------------------------ | ------------------------ | -------- | -------------------- | -------------------------------------------------------------------------------------------------------- | -------- |
| C1_1, C1_2, C1_3, C2_1, C2_2, C2_3, C4_1, C4_2, C4_3, C5_1, C5_2, C5_3, C16, C24_1, C24_2, C24_3   | 0805            | 100nF | YAGEO                                | CC0805KRX7R9BB104        | JLCPCB   | C49678               | 50V 100nF X7R ±10% 0805 Multilayer Ceramic Capacitors MLCC - SMD/SMT ROHS                                | 16       |
| C3_1, C3_2, C3_3                                                                                   | 0805            | 220nF | Samsung Electro-Mechanics            | CL21B224KBFNNNE          | JLCPCB   | C5378                | 50V 220nF X7R ±10% 0805 Multilayer Ceramic Capacitors MLCC - SMD/SMT ROHS                                | 3        |
| C6_1, C6_2, C6_3, C7_1, C7_2, C7_3, C15, C17, C18, C19, C20, C21, C22, C23                         | 0805            | 4.7uF | Samwha Capacitor                     | CS2012X7R475K350NRE      | JLCPCB   | C560882              | 35V 4.7uF X7R ±10% 0805 Multilayer Ceramic Capacitors MLCC - SMD/SMT ROHS                                | 14       |
| C8_1, C8_2, C8_3, C9_1, C9_2, C9_3, C10_1, C10_2, C10_3, C11, C12, C13, C14                        | 1206            | 47uF  | TDK                                  | C3216X5R1E476MTJ00E      | JLCPCB   | C76659               | 25V 47uF X5R ±20% 1206 Multilayer Ceramic Capacitors MLCC - SMD/SMT ROHS                                 | 13       |
| D1, D2                                                                                             | 0805            |       | Hubei KENTO Elec                     | C2297                    | JLCPCB   | C2297                | 0805 Light Emitting Diodes (LED) ROHS                                                                    | 2        |
| H1, H2, H3, H4, H5                                                                                 | HOLE_M3         |       |                                      |                          |          |                      | Hole M3                                                                                                  | 5        |
| P1                                                                                                 | DC-005 2.0      |       | BOOMELE(Boom Precision Elec)         | DC-005 2.0               | JLCPCB   | C16214               | Shrouded DC Power Receptacle 2mm 6.4mm Plugin AC/DC Power Connectors ROHS                                | 1        |
| P2, P3, P4                                                                                         | 1727036         |       | Phoenix Contact                      | 1727036                  | JLCPCB   | C457200              | TERM BLK 4P SIDE ENT 3.81MM PCB                                                                          | 3        |
| P5                                                                                                 | 1727010         |       | Phoenix Contact                      | 1727010                  | JLCPCB   | C89123               | TERM BLK 2P SIDE ENT 3.81MM PCB                                                                          | 1        |
| P6                                                                                                 | PZ254V-11-05P   |       | XFCN                                 | PZ254V-11-05P            | JLCPCB   | C492404              | Straight Square Pins 2.5mm 6mm -40℃~+105℃ 3mm 5 2.54mm Black Brass 1x5P Plugin,P=2.54mm Pin Headers ROHS | 1        |
| P7, P8, P9_1, P9_2                                                                                 | HEADER 3X2      |       | BOOMELE(Boom Precision Elec)         | C65114                   | JLCPCB   | C65114               | Straight 2 6 2.54mm Black Straight,P=2.54mm Pin Headers ROHS                                             | 4        |
| P10                                                                                                | TYPE-C-31-M-12  |       | Korean Hroparts Elec                 | TYPE-C-31-M-12           | JLCPCB   | C165948              | USB C SMD Connector                                                                                      | 1        |
| Q1, Q2                                                                                             | SOT-23-3        |       | JSMSEMI                              | S8050                    | JLCPCB   | C916390              | 25V 300mW 500mA SOT-23 Bipolar Transistors - BJT ROHS                                                    | 2        |
| R1_1, R1_2, R1_3, R9, R11, R12, R14_1, R14_2, R14_3, R15_1, R15_2, R15_3, R16_1, R16_2, R16_3, R21 | 0805            | 10K   | UNI-ROYAL(Uniroyal Elec)             | 0805W8F1002T5E           | JLCPCB   | C17414               | 125mW Thick Film Resistors ±1% 10kΩ 0805 Chip Resistor - Surface Mount ROHS                              | 16       |
| R2_1, R2_2, R2_3                                                                                   | 0805            | 0R    | PANASONIC                            | ERJ6GEY0R00V             | JLCPCB   | C169855              | 125mW 0Ω 0805 Chip Resistor - Surface Mount ROHS                                                         | 3        |
| R3_1, R3_2, R3_3, R5_1, R5_2, R5_3                                                                 | 0805            | 50m   | YAGEO                                | PE0805FRF7W0R05L         | JLCPCB   | C858613              | 250mW ±1% 50mΩ 0805 Chip Resistor - Surface Mount ROHS                                                   | 6        |
| R4_1, R4_2, R4_3, R6_1, R6_2, R6_3                                                                 | 0805            | 100K  | FH (Guangdong Fenghua Advanced Tech) | RS-05K104JT              | JLCPCB   | C118844              | 125mW ±5% 100kΩ 0805 Chip Resistor - Surface Mount ROHS                                                  | 6        |
| R8                                                                                                 | 0805            | 1K6   | Resistor.Today                       | AECR0805F1K60K9          | JLCPCB   | C352253              | 125mW Thick Film Resistors ±1% 1.6kΩ 0805 Chip Resistor - Surface Mount ROHS                             | 1        |
| R10, R13, R17, R22                                                                                 | 0805            | 470R  | UNI-ROYAL(Uniroyal Elec)             | 0805W8F4700T5E           | JLCPCB   | C17710               | 125mW Thick Film Resistors ±1% 470Ω 0805 Chip Resistor - Surface Mount ROHS                              | 4        |
| R18                                                                                                | 0805            | 5.1M  | TA-I Tech                            | RM10FTN5104              | JLCPCB   | C156163              | 125mW Thick Film Resistors ±1% 5.1MΩ 0805 Chip Resistor - Surface Mount ROHS                             | 1        |
| R19, R20                                                                                           | 0805            | 2K2   | LIZ Elec                             | CR0805J80222G            | JLCPCB   | C101970              | 125mW Thick Film Resistors ±5% 2.2kΩ 0805 Chip Resistor - Surface Mount ROHS                             | 2        |
| S1, S3                                                                                             | PUSHBUTTON_2    |       | C&K                                  | PTS645SM43SMTR92LFS      | JLCPCB   | C221880              | SWITCH TACTILE SPST-NO 0.05A 12V                                                                         | 2        |
| S2_1, S2_2, S2_3                                                                                   | SDA03H0SBR      |       | C&K                                  | SDA03H0SBR               | JLCPCB   | C221950              | SWITCH SLIDE DIP SPST 25MA 24V                                                                           | 3        |
| TP1, TP2, TP3, TP4, TP5                                                                            | 5015            |       | Ronghe                               | RH-5015                  | JLCPCB   | C5199798             | Thimble/Copper Rod/Test Ring ROHS                                                                        | 5        |
| U1_1, U1_2, U1_3                                                                                   | 28-QFN          |       | Allegro MicroSystems, LLC            | A4988SETTR-T             | JLCPCB   | C38437               | IC MTR DRVR BIPOLAR 3-5.5V 28QFN                                                                         | 3        |
| U2                                                                                                 | ESP32-WROOM-32E |       | Espressif Systems                    | ESP32-WROOM-32E-N4       | JLCPCB   | C701341              | RX TXRX MOD WIFI TRACE ANT SMD                                                                           | 1        |
| U3                                                                                                 | CP2102N         |       | SILICON LABS                         | CP2102N-A02-GQFN28R      | JLCPCB   | C964632              | QFN-28 USB ICs ROHS                                                                                      | 1        |
| U4                                                                                                 | SOT-223         |       | Shenzhen Fuman Elec                  | AMS1117-3.3V             | JLCPCB   | C173386              | IC-1117 V.reg. 1A 3V3 SOT223 SMD Ams                                                                     | 1        |


# Fabrication Instructions
>[Table of contents](#table-of-contents)


The fabrication instructions can be found in [here](./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/Lens-Maker_Fabrication_Instructions.PDF) and the Gerber files are located in [this directory](./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/GerberX2/). For the PCBA the assembly drawing can be found [here](./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/Lens-Maker_Assembly_Drawings.PDF).

<img src="./docs/Lens-Maker_Fabrication_Instructions-1.png" width="1000" >


## 3D Model
>[Table of contents](#table-of-contents)


A 3D model of the PCB is available for the design and manufacture of the lathe casing located in [here](./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/ExportSTEP/Lens-Maker_3D_STEP.step).

## Some pictures
>[Table of contents](#table-of-contents)


<img src="./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/PCB%203D%20Print/Lens-Maker_ISO2.png" width="600" >
<img src="./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/PCB%203D%20Print/Lens-Maker_ISO.png" width="600" >
<img src="./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/PCB%203D%20Print/Lens-Maker_TOP.png" width="600" >
<img src="./Lens-Maker/Project%20Outputs%20for%20Lens-Maker/PCB%203D%20Print/Lens-Maker_BOT.png" width="600" >

# Contributing
>[Table of contents](#table-of-contents)

Please do not hesitate to reach out to me if you find any issue with the code or if you have any questions.

* Personal email: [ianczdiaz@gmail.com](mailto:ianczdiaz@gmail.com)

* LinkedIn Profile: [https://www.linkedin.com/in/iancraz/](https://www.linkedin.com/in/iancraz/)

# License
>[Table of contents](#table-of-contents)

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" width="200" src="./docs/by-nc-sa.png" /></a><br />

```
Copyright 2023 Ian Cruz Diaz. 

This project and all its components, including the PCB design files, Schematics and Output Files are 
licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License. You 
can find a copy of the License at ./LICENSE.md or at https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.
```


