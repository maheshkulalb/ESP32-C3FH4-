# ESP32-C3FH4 Development Board (External Antenna)
<img width="2272" height="1264" alt="ESP2" src="https://github.com/user-attachments/assets/faa2172d-a2d7-48fe-9d1d-561b2305a053" />
<img width="2272" height="1264" alt="ESP3" src="https://github.com/user-attachments/assets/ba98501c-5963-403d-b2a7-006f031d0636" />
<img width="2272" height="1264" alt="ESP1" src="https://github.com/user-attachments/assets/b2d07cf0-756b-4318-b9c9-4996b8f62a49" />

## Overview
This repository contains the complete open-source hardware design for a custom development board based on the Espressif **ESP32-C3FH4** SoC (RISC-V 32-bit single-core, integrated 4MB Flash). 

Unlike standard modules that rely on a PCB trace antenna, this design specifically routes the RF path to an external antenna connector , making it ideal for deployments inside metal enclosures or applications requiring higher-gain antennas. 


## Key Features
* **Microcontroller:** ESP32-C3FH4 (RISC-V 32-bit, 160MHz, built-in 4MB Flash)
* **Connectivity:** 2.4 GHz Wi-Fi and Bluetooth 5 (LE)
* **RF Interface:** connector with impedance-matched 50Ω RF routing
* **USB Interface:** USB Type-C for power and direct Serial flashing
* **Power Supply:** 5V to 3.3V LDO regulator 
* **I/O Breakout:** Standard 2.54mm pitch headers 
* **User Interface:** Reset button, User Boot button (GPIO9)

## EDA Tool & Source Files
This project is designed entirely in **KiCad** 

The native KiCad project files are included, allowing you to modify the schematics, tweak the PCB layout, or export custom manufacturing files.

### Repository Structure
* `/Hardware` - Native KiCad project files (`.kicad_pro`, `.kicad_sch`, `.kicad_pcb`)
* `/Gerbers` - Ready-to-manufacture Gerber and Drill files

**Recommended Fabrication Specs:**
* **Layers:4**
* **Thickness:1.57mm**
* **Impedance Control:Yes**


You are free to use, modify, and distribute this design
