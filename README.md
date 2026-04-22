# ESP32-C3FH4 Development Board (External Antenna)

<img width="2272" height="1264" alt="esp1" src="https://github.com/user-attachments/assets/ecd23b95-ca5b-4fec-a129-b9fc96139d3d" />
<img width="2272" height="1264" alt="esp4" src="https://github.com/user-attachments/assets/1fb541e4-335c-462e-a922-0dc724906caa" />
<img width="2272" height="1264" alt="esp3" src="https://github.com/user-attachments/assets/50b7d080-c7c6-4ed5-b6eb-13c65060ba93" />
<img width="2272" height="1264" alt="esp2" src="https://github.com/user-attachments/assets/b80a8338-b15b-4e7b-9557-5770cd2770d3" />
*3D render of the assembled PCB.*

## Overview
This repository contains the complete open-source hardware design for a custom development board based on the Espressif **ESP32-C3FH4** SoC (RISC-V 32-bit single-core, integrated 4MB Flash). 

Unlike standard modules that rely on a PCB trace antenna, this design specifically routes the RF path to an external antenna connector (U.FL/SMA), making it ideal for deployments inside metal enclosures or applications requiring higher-gain antennas. 

## Key Features
* **Microcontroller:** ESP32-C3FH4 (RISC-V 32-bit, 160MHz, built-in 4MB Flash)
* **Connectivity:** 2.4 GHz Wi-Fi and Bluetooth 5 (LE)
* **RF Interface:** `[U.FL / SMA]` connector with impedance-matched 50Ω RF routing
* **USB Interface:** USB Type-C for power and direct native USB-to-JTAG/Serial flashing
* **Power Supply:** 5V to 3.3V LDO regulator (`[Insert LDO part number, e.g., AMS1117-3.3 or ME6211]`) with reverse polarity protection
* **I/O Breakout:** Standard 2.54mm pitch headers exposing all available GPIOs, SPI, I2C, and UART
* **User Interface:** Reset button, User Boot button (GPIO9), and RGB WS2812B LED (GPIO8)

## EDA Tool & Source Files
This project is designed entirely in **KiCad** `[Insert Version, e.g., 7.0 / 8.0]`. 

The native KiCad project files are included, allowing you to modify the schematics, tweak the PCB layout, or export custom manufacturing files.

### Repository Structure
* `/Hardware` - Native KiCad project files (`.kicad_pro`, `.kicad_sch`, `.kicad_pcb`)
* `/Gerbers` - Ready-to-manufacture Gerber and Drill files
* `/BOM` - Bill of Materials (CSV) and Centroid/CPL files for PCBA pick-and-place
* `/Docs` - PDF exports of the schematic and interactive HTML BOM
* `/3D_Models` - STEP files of the completed board for mechanical enclosure design

## Design Notes: RF & Signal Integrity
Special attention was given to the RF routing between the ESP32-C3FH4 LNA/PA pin and the antenna connector. 
* A Pi-network footprint is included for fine-tuning the antenna impedance matching.
* Trace width and clearance were calculated for a 50Ω characteristic impedance based on a `[Insert PCB thickness, e.g., 1.6mm]` FR4 stackup from standard board houses. 
* Adequate ground via stitching is implemented along the RF path to minimize EMI and signal loss.

## Manufacturing & Assembly
The files in the `/Gerbers` and `/BOM` directories are formatted for seamless submission to standard rapid prototyping services (like JLCPCB or PCBWay). 

**Recommended Fabrication Specs:**
* **Layers:4
* **Thickness:1.57mm
* **Impedance Control:Yes

## License
This hardware design is released under the **[Insert Chosen License, e.g., CERN Open Hardware Licence Version 2 - Permissive (CERN-OHL-P)]**. 

You are free to use, modify, and distribute this design, including for commercial manufacturing, provided you include the original attribution.
