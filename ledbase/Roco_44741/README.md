# LEDbase: Roco #44741
[![Real-time Bus (RTB)](https://img.shields.io/badge/RTB_Project-FF6699)](https://www.rtb4dcc.de)
[![Kicad_Libs](https://img.shields.io/badge/Kicad_Libs-29C7FF)](https://github.com/git4dcc/RTB_SamacSys)
[![Apache License 2.0](https://img.shields.io/badge/license-Apache%20License%202.0-lightgray)](https://www.apache.org/licenses/LICENSE-2.0)

LED base carier for H0 Roco #44741 to be used with RTB_D99.
PCB contains LEDs for ilse, cabin and lavatory. In addition, external tail light LEDs can be attached on each end.

<br>

> [!CAUTION]
> This project is **work in progress** and there may be (hope not) changes to the overall design if the current turns out to be not practical.

<br>

<img src="supplemental/images/D99a_main.jpg">
<br>

## LED base features
- **LED ports**
  - 4x 74HC595 shift register
  - 31 individual LEDs
- SUSI 3.3V
- 2.8V SCAP (optional)
- 16V Polymer Caps (optional)
- ambient light sensor (optional)

# Hardware
The current PCB layout uses SMD footprints. Reflow soldering is recommended.

<img src="supplemental/images/D99a_top.jpg">
<img src="supplemental/images/D99a_btm.jpg">

## PCB
- 2-layer PCB, FR4, 1mm
- CPU: none

<details>
<summary>Details</summary>


## Kicad
[Schematic](doc/D99a_schematic.pdf) | [Layout](doc/D99a_layout.pdf) | [Gerber](gerber)


:yellow_circle: Requires my Kicad project library [RTB_SamacSys](https://github.com/git4dcc/RTB_SamacSys) in the same directory tree.

</details>


# Images
<img src="supplemental/images/D99a_usecase2.jpg" width=365> <img src="supplemental/images/D99a_usecase1.jpg" width=630>
<img src="supplemental/images/D99a_w_ctl.jpg">

This project is intended for hobby use only and is distributed in accordance with the Apache License 2.0 agreement.
