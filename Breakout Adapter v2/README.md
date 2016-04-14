## V2 - UART Adapter

### Changelog/Updates:
**No updates yet**

### Pictures
V2.0A - Bare PCB<br />
<img src="https://github.com/8n1/ESP8266-Breakout-Adapter/blob/master/Breakout%20Adapter%20v1.1%20-%20LM1117/Pictures%20(PCB)/ESP12E%20Breakout%20Adapter%20-%20V1-0.jpeg" width="600" alt="ESP-12 Breakout Adapter V1.0 - Bare PCB" />
<br />
V2.0A - OSH Park renderings<br />
<img src="https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/155e047f43987161602c911e067b01d4.png" width="300" alt="ESP-12 Breakout Adapter V1.1 - Front" />&nbsp;
<img src="https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/1fb6627899a7fd7488e3e4fad130234f.png" width="300" alt="ESP-12 Breakout Adapter V1.1 - Back" />
<br />
### Schematic
<img src="https://raw.githubusercontent.com/8n1/ESP8266-Breakout-Adapter/master/Breakout%20Adapter%20v2.0A%20-%20AS1363/ESP%20Breakout%20Adapter%20-%20v2_0A%20-%20AS1363_schematic.png" width="600" alt="ESP-12 Breakout Adapter V1.1 - Schematic" />


### Features
* ESP-07, ESP-12, ESP-12E and ESP-12F compatible (bottom header for E and F module is not brought out)
* On-board voltage regulator
* Flash and Reset switch
* Pullup resistors for Reset, CH_PD and GPIO0
* Pulldown resistor for GPIO15
* UART Programming Header (With Reset and GPIO0)
* "Sensor Header" (1.27mm) with pullup resistors (Pinout: 3V3, GPIO12, GPIO14, GND)
* LDO Enable Pin brought out * + footprint for a pullup or pulldown resistor on-board 
* DeepSleep wake-up jumper - Connects Pin8 and Pin32 and allows automatic deep-sleep wake-up
* On-board LED - Anode(+) can either be connected to the LDO ouptut(3V3) or GPIO13 - selected using solderjumper "Led cfg"
* 2 Mountingholes (2.0mm)
* Expect for the "Sensor" and UART header breadboard compatible -> 2 rows stay free
* Except for the headers, fully SMD

\* Can be used to completly shutdown the board and everything connected to it. The current consumption in this state will typically be &lt;1µA. 

### Partlist (v2.0)
| Part  | Value                      | Info                |
|:------|:---------------------------|:--------------------|
| IC1   | SPX3819M5-L-3-3 (SOT23-5) | Voltage regulator - Variant "A" |
| IC1   | AS1363-BSTT-33 (SOT23-6)  | Voltage regulator - Variant "B" |
| C1    | 10µF (Ceramic, 1206)      | Input capacitor for IC1 |
| C2    | 10µF (Ceramic, 1206)      | Output capacitor for IC1 |
| <del>C3</del>    | <del>10nF Ceramic 0805</del>      | <del>Bypass capacitor for IC1</del> (not needed) |
| C4    | 100nF (Ceramic, 0805)n    | Decoupling capacitor for the ESP module |
| R1    | 10K (0805) *              | Pullup resistor for CH_PD  |
| R2    | 10K (0805) *              | Pulldown resistor for GPIO15  |
| R3    | 10K (0805)                | Pullup resistor for Reset |
| R4    | 10K (0805)                | Pullup resistor for GPIO0 |
| R5/R8 | 10K-100K (0805)           | Pullup OR Pulldown for the LDO enable pin |
| R9    | 10K (0805)                | [Optional] Pullup resistor for GPIO12 |
| R10   | 10K (0805)                | [Optional] Pullup resistor for GPIO14 |
| R7    | ~220 Ohm (0805)           | [Optional] Current limiting resistor for the led ** |
| LED   | LED (0805)                | [Optional] Led of choice ** |
| DS    | Solderbridge       | DeepSleep wake-up jumper |
| FLASH | Tactile Pushbutton, SMD 2pin 6x3       | Flash button |
| RESET | Tactile Pushbutton, SMD 2pin 6x3       | Reset button |

\* **or** 0Ohm resistor/solderbridge if pin is not needed<br /> 
\** if the led is connected to GPIO13 the led current must be lower then 12mA, calculate the resister value accordingly!

Pinheader
* 1x 1x10 (2.54mm)
* 1x 1x11 (2.54mm)
* 1x 1x6 (2.54mm) - right angle pin header

Optional "socket" header for the esp module
* 2x 1x8 (2mm) female and male

### Difference between variant A and B
The only difference is the used LDO. Variant A uses the AS1363, variant B the SPX3819(or pincompatible).

#### Resources:
- AS1363 Datasheet - https://ams.com/eng/content/download/1961/15107/file/AS1364_Datasheet_EN_v3.pdf
- SPX3819 Datasheet - https://www.adafruit.com/datasheets/SPX3819_DS_R202_052014.pdf

- More Pictures V2.0 - http://imgur.com/a/XCGv0 (imgur album)

#### This adapter on OSH Park:
- ESP8266 Breakout v2.0A - https://oshpark.com/shared_projects/2IkxaFPm
- ESP8266 Breakout v2.0B - https://oshpark.com/shared_projects/jsl8ZcFp

#### License
<img src="http://mirrors.creativecommons.org/presskit/buttons/88x31/png/by.png" alt="Creative Commons License - BY" /><br />
Creative Commons Attribution 4.0 International<br />
http://creativecommons.org/licenses/by/4.0/