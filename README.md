# RTB_D99
[![Real-time Bus (RTB)](https://img.shields.io/badge/RTB_Project-FF6699)](https://www.rtb4dcc.de)
[![Kicad_Libs](https://img.shields.io/badge/Kicad_Libs-29C7FF)](https://github.com/git4dcc/RTB_SamacSys)
[![Apache License 2.0](https://img.shields.io/badge/license-Apache%20License%202.0-lightgray)](https://www.apache.org/licenses/LICENSE-2.0)

My Homebrew D99 decoder core is designed to drive various custom made LED strips. The core can address up to 32 individual LEDs and 4 AUX ports. The D99 itself has no LEDs nor does it have any buffer capacitors. The D99 only implements the charging logic for polymer or supercaps to be attached externally.


> [!CAUTION]
> This project is **work in progress** and there may be (hope not) changes to the overall design if the current turns out to be not practical.


<details>
<summary>User Guides</summary>

- User Guide - DE
- [User Guide - EN](https://rtb4dcc.de/rtb_decoder_reference_en/)

</details>

<img src="supplemental/images/D99_main.jpg" width=700>
<br>

## Decoder features
- **DCC**
  - DCC-A automatic logon
  - DCC-R protocol extension
  - Service Mode Programming
- **Railcom**
  - Channel 1/2
  - POM, xPOM
  - DYN: QoS, Track-Voltage, Scap-Voltage, Temp, Ambient light
- **AUX ports**
  - 4 AUX ports (3.3V logic level)
  - AUX ports my be used for Servo
- **LED ports**
  - designed for 74HC595 shift register usage
  - allows up to 32 individual LEDs
- SUSI 3.3V
- 2.8V SCAP (optional, external to PCB)
- 16V Polymer Caps (optional, external to PCB)
- Inrush limited
- max track voltage 25V
- CPU heartbeat LED
- ambient light sensor (optional)
- fast firmware update within seconds on main tracks via DCC-R

# Hardware
The current PCB layout uses SMD footprints with 0.4mm pitch and mainly 0402 parts. Reflow soldering is mandatory.
The layout has been optimized to automatic PCB assembly.

| top | bottom |
| --- | --- |
| <img src="supplemental/images/D99_top.jpg"> | <img src="supplemental/images/D99_btm.jpg"> |

## PCB
- 4-layer PCB, FR4, 1mm
- CPU: AVR64DA48

<details>
<summary>Details</summary>

<img src="supplemental/images/D99_pinout.jpg" width=50%>

</details>

## Kicad
[Schematic](doc/D99_schematic.pdf) | [Layout](doc/D99_layout.pdf) | [Gerber](gerber)

<details>
<summary>Dependency</summary>
<br>

:yellow_circle: Requires my Kicad project library [RTB_SamacSys](https://github.com/git4dcc/RTB_SamacSys) in the same directory tree.

</details>


## Firmware
Filename structure: { **pcb** }{ **code** }{ **version** }.hex

Example: **D99F0001**.hex

|   | Description |
| --- | --- |
| **pcb** | Name of matching hardware (**D99**) |
| **code** | Type of code contained (**R**=rom, **B**=bootloader, **F**=flash, **U**=bld update, **P**=UPDI factory code) |
| **version** | Release version (**####**) |

[Firmware files](firmware)

## UPDI
The fuse settings as well as the P-code (D99Pxxxx.hex) has to be installed by using UPDI.<br>

> to be done ...

# Images
<img src="supplemental/images/D99_usecase1.jpg" width=300> <img src="supplemental/images/D99_usecase2.jpg" width=508>

# YouTube
See the D99 decoder core prototype in action piggyback on a LED test carrier.<br><br>
[<img src="https://img.youtube.com/vi/czScUCT7jxQ/0.jpg" width=30%>](https://www.youtube.com/watch?v=czScUCT7jxQ) [<img src="https://img.youtube.com/vi/SbPsQP1knIc/0.jpg" width=30%>](https://www.youtube.com/watch?v=SbPsQP1knIc)

This project is intended for hobby use only and is distributed in accordance with the Apache License 2.0 agreement.
