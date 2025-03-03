
# Panasonic Q Replacement Remote

[![GitHub](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

A low-cost (~$30 USD BOM) replacement remote for the Panasonic Q (N2QAJB000034)

# Order Information

### Ordering the PCB

<ins>**With Assembly**</ins>

Todo

<ins>**Without Asembly**</ins>

Todo

### Ordering the enclosure
Todo

### Ordering the button panel
1. Navigate to [LCSC's Front Panel order page](https://www.lcsc.com/front-panel/custom-quote)
2. Click `Please Order Now`
3. Click the plus icon under PET Front Panel custom-quote
4. Upload the `Button Cover Production Files.zip` file 
5. Enter your desired quantity (The price difference between 1 and 5 is low, i suggest getting 5 just in case)
6. Press `Please Order Now`
7. When LCSC emails you the quote, make sure you tell them you want 0.125mm or 0.2mm thickness with 3M9448A adhesive backing

# Programming
### Tools & Software Needed
- An SWD programmer like the STLink V2
- [STM32CubeProgrammer](https://www.st.com/en/development-tools/stm32cubeprog.html)
### Programming
1. Connect the programmer to the circuitboard (according to the pinout written on the programmer and the board)
2. Open STM32CubeProgrammer
3. Press the open file button and select `Panasonic-Q-Remote-Firmware.elf`
4. Select ST-Link in the drop down on the right and click connect
5. Click `Download` to flash the firmware

# Parts Overview
## Enclosure Parts
```
1x Panasonic Q Remote Top Half
1x Panasonic Q Remote Bottom Half
1x Panasonic Q Remote Button Cover
4x M3x8 countersunk screws
4x M3x10 countersunk screws
4x M3x3x4.5mm threaded insert
4x M3x5x4.5mm threaded insert
4x 5x2mm round rubber feet (optional)
```

## Board Parts
|        Designator       | Qty |    Part Number   |     Package     |     Description    | LCSC Part |
|:-----------------------:|:---:|:----------------:|:---------------:|:------------------:|:-----------:|
|            U1           |  1  |   STM32L412KBT6  |   LQFP-32(7x7)  |                    | [C529438](https://www.lcsc.com/product-detail/Microcontrollers-MCU-MPU-SOC_STMicroelectronics-STM32L412KBT6_C529438.html) |
|         C1,C2,C3        |  3  |                  |       0603      |   100nF Capacitor  | [C14663](https://www.lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_YAGEO-CC0603KRX7R9BB104_C14663.html) |
| R1,R2,R3,R4,R5,R6,R7,R8 |  8  |                  |       0603      |    10KΩ Resistor   | [C98220](https://www.lcsc.com/product-detail/Chip-Resistor-Surface-Mount_YAGEO-RC0603FR-0710KL_C98220.html) |
|            R9           |  1  |                  |       0603      |    1KΩ Resistor    | [C22548](https://www.lcsc.com/product-detail/Chip-Resistor-Surface-Mount_YAGEO-RC0603FR-071KL_C22548.html) |
|           R10           |  1  |                  |       0603      |    100Ω Resistor   | [C105588](https://www.lcsc.com/product-detail/Chip-Resistor-Surface-Mount_YAGEO-RC0603FR-07100RL_C105588.html) |
|         SW1-SW41        |  41 |     B3S-1000     |                 |   Tactile Switch   | [C2733655](https://www.lcsc.com/product-detail/Tactile-Switches_Omron-Electronics-B3S-1000_C2733655.html) |
|           BT1           |  1  |   BH-AA-B5BA034  |                 |  AA Battery Holder | [C20606806](https://www.lcsc.com/product-detail/Button-And-Strip-Battery-Connector_MYOUNG-BH-AA-B5BA034_C20606806.html) |
|            D1           |  1  | IR204-A-L(BY)(M) | Plugin,P=2.54mm |     3mm IR Led     | [C17179477](https://www.lcsc.com/product-detail/Infrared-LED-Emitters_Everlight-Elec-IR204-A-L-BY-M_C17179477.html) |
|            Q1           |  1  |      2N3904X     |      TO-92      | NPN BJT Transistor | [C5156722](https://www.lcsc.com/product-detail/Bipolar-BJT_Shenzhen-JingYang-2N3904X_C5156722.html) |


## Remote Codes
|        Button        | Address | Command |
|:--------------------:|:-------:|:-------:|
|         Stop         |  0x26A  |   0x0   |
| Slow/Search Backward |  0x26A  |   0x2   |
|  Slow/Search Forward |  0x26A  |   0x3   |
|         Pause        |  0x26A  |   0x6   |
|      DVD/CD Play     |  0x26A  |   0xA   |
|           1          |  0x26A  |   0x10  |
|           2          |  0x26A  |   0x11  |
|           3          |  0x26A  |   0x12  |
|           4          |  0x26A  |   0x13  |
|           5          |  0x26A  |   0x14  |
|           6          |  0x26A  |   0x15  |
|           7          |  0x26A  |   0x16  |
|           8          |  0x26A  |   0x17  |
|           9          |  0x26A  |   0x18  |
|           0          |  0x26A  |   0x19  |
|       Surround       |  0x26A  |   0x30  |
|         Mute         |  0x26A  |   0x32  |
|         Audio        |  0x26A  |   0x33  |
|          Up          |  0x26A  |   0x34  |
|         Down         |  0x26A  |   0x35  |
|         Right        |  0x26A  |   0x36  |
|         Left         |  0x26A  |   0x37  |
|         Power        |  0x26A  |   0x3D  |
|        Repeat        |  0x26A  |   0x47  |
|      A-B Repeat      |  0x26A  |   0x48  |
|     Skip Backward    |  0x26A  |   0x49  |
|     Skip Forward     |  0x26A  |   0x4A  |
|        Display       |  0x26A  |   0x57  |
|        Cancel        |  0x26A  |   0x80  |
|          >10         |  0x26A  |   0x84  |
|         Game         |  0x26A  |   0xA6  |
|       Top Menu       |  0x26A  |   0xAB  |
|        Marker        |  0x26A  |   0xAC  |
|         Angle        |  0x26A  |   0xAD  |
|       Subtitle       |  0x26A  |   0xAE  |
|      Preferences     |  0x26A  |   0xB5  |
|      Game Timer      |  0x26A  |   0x96  |
|      Playback Mode   |  0x26A  |   0xBB  |
|         Menu         |  0x26A  |   0xC0  |
|        Return        |  0x26A  |   0xC4  |
|         Enter        |  0x26A  |   0xC6  |

All of the commands are 48-bit Panasonic Protocol Ir Codes


## Images

![image](https://github.com/user-attachments/assets/01a0169c-c873-45df-899e-c42dc5295cd8)

![PXL_20250226_144714669 RAW-01 COVER](https://github.com/user-attachments/assets/3ac98e4b-898f-437f-bf19-77341c2881a5)



