# RTB_D13
[![Real-time Bus (RTB)](https://img.shields.io/badge/RTB_Project-FF6699)](https://www.rtb4dcc.de)
[![Kicad_Libs](https://img.shields.io/badge/Kicad_Libs-29C7FF)](https://github.com/git4dcc/RTB_SamacSys)
[![Apache License 2.0](https://img.shields.io/badge/license-Apache%20License%202.0-lightgray)](https://www.apache.org/licenses/LICENSE-2.0)

My Homebrew [D13](https://rtb4dcc.de/hardware/decoder/d13/) LED decoder is a drop in design for Minitrix (#15791) coach with no mechanical modification required. The decoder is designed to integrate into the [RTB](https://rtb4dcc.de/concept/) digital control infrastructure.

<details>
<summary>User Guides</summary>

- User Guide - DE
- [User Guide - EN](https://rtb4dcc.de/rtb_decoder_reference_en/)

</details>

<img src="https://www.spurweite-n.de/NDBPics/Minitrix/15791.jpg" width=400>
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
- 1x4F/2.8V SCAP (on PCB)
- Inrush limited
- motor current limited to 500mA (short circuit protected)
- max track voltage 25V
- Corridor (11 LEDs), Cabin (13 LEDs), Lavatory (2 LEDs)
- CPU heartbeat LED
- motion sensor
- fast firmware update within seconds on main tracks via DCC-R

# Hardware
The current PCB layout uses SMD footprints with 0.5mm pitch and mainly 0603 parts. Reflow soldering is recommended whereas handsoldering will be difficult.

<img src="https://rtb4dcc.de/wp-content/uploads/2023/06/D13_top.jpg" width=800>
<img src="https://rtb4dcc.de/wp-content/uploads/2023/06/D13_btm.jpg" width=800>

## PCB
- 4-layer PCB, FR4, 1mm
- CPU: AVR64DA48

[Schematic](doc/D13_schematic.pdf) | [Layout](doc/D13_layout.pdf)

## Kicad
[Schematic](doc/D13_schematic.pdf) | [Layout](doc/D13_layout.pdf) | [Gerber](gerber)

<details>
<summary>Dependency</summary>
<br>

:yellow_circle: Requires my Kicad project library [RTB_SamacSys](https://github.com/git4dcc/RTB_SamacSys) in the same directory tree.

</details>


## Firmware
Filename structure: { **pcb** }{ **code** }{ **version** }.hex

Example: **D13F0001**.hex

|   | Description |
| --- | --- |
| **pcb** | Name of matching hardware (**D13**) |
| **code** | Type of code contained (**R**=rom, **B**=bootloader, **F**=flash, **U**=bld update, **P**=UPDI factory code) |
| **version** | Release version (**####**) |

# YouTube
See the D13 decoder in action.<br><br>
[<img src="https://img.youtube.com/vi/nAJpYsdv1IA/0.jpg" width=260>](https://youtube.com/watch?v=nAJpYsdv1IA)

This project is intended for hobby use only and is distributed in accordance with the Apache License 2.0 agreement.
