
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
|        Button        | Address | Command |    Raw Data    |
|:--------------------:|:-------:|:-------:|:--------------:|
|         Stop         |  0x26A  |   0x0   | 0x860026A02002 |
| Slow/Search Backward |  0x26A  |   0x2   | 0x840226A02002 |
|  Slow/Search Forward |  0x26A  |   0x3   | 0x850326A02002 |
|         Pause        |  0x26A  |   0x6   | 0x800626A02002 |
|      DVD/CD Play     |  0x26A  |   0xA   | 0x8C0A26A02002 |
|           1          |  0x26A  |   0x10  | 0x961026A02002 |
|           2          |  0x26A  |   0x11  | 0x971126A02002 |
|           3          |  0x26A  |   0x12  | 0x941226A02002 |
|           4          |  0x26A  |   0x13  | 0x951326A02002 |
|           5          |  0x26A  |   0x14  | 0x921426A02002 |
|           6          |  0x26A  |   0x15  | 0x931526A02002 |
|           7          |  0x26A  |   0x16  | 0x901626A02002 |
|           8          |  0x26A  |   0x17  | 0x911726A02002 |
|           9          |  0x26A  |   0x18  | 0x9E1826A02002 |
|           0          |  0x26A  |   0x19  | 0x9F1926A02002 |
|       Surround       |  0x26A  |   0x30  | 0xB63026A02002 |
|         Mute         |  0x26A  |   0x32  | 0xB43226A02002 |
|         Audio        |  0x26A  |   0x33  | 0xB53326A02002 |
|          Up          |  0x26A  |   0x34  | 0xB23426A02002 |
|         Down         |  0x26A  |   0x35  | 0xB33526A02002 |
|         Right        |  0x26A  |   0x36  | 0xB03626A02002 |
|         Left         |  0x26A  |   0x37  | 0xB13726A02002 |
|         Power        |  0x26A  |   0x3D  | 0xBB3D26A02002 |
|        Repeat        |  0x26A  |   0x47  | 0xC14726A02002 |
|      A-B Repeat      |  0x26A  |   0x48  | 0xCE4826A02002 |
|     Skip Backward    |  0x26A  |   0x49  | 0xCF4926A02002 |
|     Skip Forward     |  0x26A  |   0x4A  | 0xCC4A26A02002 |
|        Display       |  0x26A  |   0x57  | 0xD15726A02002 |
|        Cancel        |  0x26A  |   0x80  |  0x68026A02002 |
|          >10         |  0x26A  |   0x84  |  0x28426A02002 |
|         Game         |  0x26A  |   0xA6  | 0x20A626A02002 |
|       Top Menu       |  0x26A  |   0xAB  | 0x2DAB26A02002 |
|        Marker        |  0x26A  |   0xAC  | 0x2AAC26A02002 |
|         Angle        |  0x26A  |   0xAD  | 0x2BAD26A02002 |
|       Subtitle       |  0x26A  |   0xAE  | 0x28AE26A02002 |
|      Preferences     |  0x26A  |   0xB5  | 0x33B526A02002 |
|      Game Timer      |  0x26A  |   0x96  | 0x109626A02002 |
|      Playback Mode   |  0x26A  |   0xBB  | 0x3DBB26A02002 |
|         Menu         |  0x26A  |   0xC0  | 0x46C026A02002 |
|        Return        |  0x26A  |   0xC4  | 0x42C426A02002 |
|         Enter        |  0x26A  |   0xC6  | 0x40C626A02002 |