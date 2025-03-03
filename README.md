
# Panasonic Q Replacement Remote

[![GitHub](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)

A cheap(ish) replacement remote for the Panasonic Q (N2QAJB000034)

# Order Information

### Ordering the board

<ins>**With Assembly**</ins>

Todo

<ins>**Without Asembly**</ins>

Todo

### Ordering the enclosure
Todo

### Ordering the button panel

Todo

# Programming the circuitboard
### Tools & Software Needed
- An SWD programmer like the STLink V2
- [STM32CubeProgrammer](https://www.st.com/en/development-tools/stm32cubeprog.html)
### Programming
1. Connect the programmer to the circuitboard (according to the pinout written on the programmer and the board)
2. Open STM32CubeProgrammer
3. Press the open file button and select `PanasonicQRemoteFirmware.elf`
4. Select ST-Link in the drop down on the right and click connect
5. Press Download

# Parts overview
## Enclosure Parts
```
1x Panasonic Q Remote Top Half
1x Panasonic Q Remote Bottom Half
1x Panasonic Q Remote Top Half
1x Panasonic Q Remote Button Cover
4x M3x8 countersunk screws
4x M3x10 countersunk screws
4x M3x3x4.5mm threaded insert
4x M3x5x4.5mm threaded insert
4x 5x2mm round rubber feet (optional)
```

## Circuitboard Parts
|        Designator       | Qty |    Part Number   |     Package     |     Description    |
|:-----------------------:|:---:|:----------------:|:---------------:|:------------------:|
|            U1           |  1  |   STM32L412KBT6  |   LQFP-32(7x7)  |                    |
|         C1,C2,C3        |  3  |                  |       0603      |   100nF Capacitor  |
| R1,R2,R3,R4,R5,R6,R7,R8 |  8  |                  |       0603      |    10KΩ Resistor   |
|            R9           |  1  |                  |       0603      |    1KΩ Resistor    |
|           R10           |  1  |                  |       0603      |    100Ω Resistor   |
|         SW1-SW41        |  41 |     B3S-1000     |                 |   Tactile Switch   |
|           BT1           |  1  |   BH-AA-B5BA034  |                 |  AA Battery Holder |
|            D1           |  1  | IR204-A-L(BY)(M) | Plugin,P=2.54mm |     3mm IR Led     |
|            Q1           |  1  |      2N3904X     |      TO-92      | NPN BJT Transistor |


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

> Uses the Panasonic IR Protocol


## Images

![image](https://github.com/user-attachments/assets/01a0169c-c873-45df-899e-c42dc5295cd8)

![PXL_20250226_144714669 RAW-01 COVER](https://github.com/user-attachments/assets/3ac98e4b-898f-437f-bf19-77341c2881a5)



