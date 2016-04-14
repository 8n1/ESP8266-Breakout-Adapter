## V3 - Mini Adapter

### Changelog/Updates: <br />

V3.1 - Nov, 2015
- Footprint for VREG input and output capacitors changed from 1206 to 0805
- VREG bypass capacitor (C3) removed
- Bigger solderpads for the tactile switches
- Pullup resistor for GPIO2 added (R7)
- Part numbers on bottom side replaced with actual values
- Layout optimized
- Silkscreen fix (description of where the led is connected to was swapped: 3V3<->GPIO13)

V3.0 - Okt, 2015
- First version

### Pictures
V3.1B - OSH Park renderings<br />
<img src="https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/ada2986226837bb70db97c0850a03c31.png" width="300" alt="ESP-12 Breakout Adapter V1.1 - Front" />&nbsp;
<img src="https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/8ab8bf034a2089dc2fbfab833ebf3101.png" width="300" alt="ESP-12 Breakout Adapter V1.1 - Back" />
<br />
### Schematic
<img src="https://raw.githubusercontent.com/8n1/ESP8266-Breakout-Adapter/master/Breakout%20Adapter%20v3/ESP%20Breakout%20Adapter%20v3.1B%20-%20SPX3819%20-%20Mini/ESP%20Breakout%20Adapter%20-%20v3_1B%20-%20SPX3819%20-%20Mini_sch.png" width="600" alt="ESP-12 Breakout Adapter V3.1 - Schematic" />


### Features
* ESP-07, ESP-12, ESP-12E and ESP-12F compatible (bottom header for E and F module is not brought out)
* On-board voltage regulator
* Flash and Reset switch
* Pullup resistors for Reset, CH_PD, GPIO0 and GPIO2
* Pulldown resistor for GPIO15
* On/Off Switch *
* LDO Enable Pin brougth out **
* DeepSleep wake-up jumper - Connects Pin8 and Pin32 and allows automatic deep-sleep wake-up
* On-board LED - Anode(+) can either be connected to the LDO ouptut ("3V3") or to "GPIO13" (selected using solderjumper)
* 2 Mountingholes (2.0mm)*)
* Expect for the headers fully SMD
* Breadboard compatible -> 3 rows stay free
* Very small

\* Can be used to completly shutdown the board and everything connected to it. The current consumption in this state will typically be &lt;1µA. 
\** Can be used to externaly turn the board on if the On/Off switch is set to "Off", or off if the On/Off switch is set to "On".

### Partlist (v3.1)
| Part  | Value                     | Info                |
|:------|:--------------------------|:--------------------|
| IC1   | SPX3819M5-L-3-3 (SOT23-5) | Voltage regulator - Variant "A" |
| IC1   | AS1363-BSTT-33 (SOT23-6) | Voltage regulator - Variant "B" |
| C1    | 10µF (Ceramic, 0805)      | Input capacitor for IC1 |
| C2    | 10µF (Ceramic, 0805)      | Output capacitor for IC1 |
| C3    | 100nF (Ceramic, 0805)     | Decoupling capacitor for the ESP module |
| R1    | 10K (0805) *              | Pullup resistor for CH_PD |
| R2    | 10K (0805) *              | Pulldown resistor for GPIO15 |
| R3    | 10K (0805)                | Pullup resistor for Reset |
| R4    | 10K (0805)                | Pullup resistor for GPIO0 |
| R7    | 10K (0805)                | Pullup resistor for GPIO2 |
| R5    | 10K (0805)                | Pullup for LDO enable pin |
| R6    | 10K (0805)                | Pulldown for LDO enable pin |
| RV    | ~220 Ohm (0805)           | [Optional] Current limiting resistor for the led ** |
| LED   | LED (0805) **             | [Optional] Led of choice |
| DS    | Solderbridge       | DeepSleep wake-up jumper |
| FLASH | Tactile Pushbutton SMD 2pin 6x3       | Flash button |
| RESET | Tactile Pushbutton SMD 2pin 6x3       | Reset button |
| On/Off | SMD slide switch (This one)       | On/Off switch |

\* **or** 0Ohm resistor/solderbridge if pin is not needed<br /> 
\** if the led is connected to GPIO13 the led current must be lower then 12mA, calculate the resister value accordingly!

Pinheader
* 2x 1x10 (2.54mm)

Optional "socket" header for the esp module
* 2x 1x8 (2mm) female and male

### Difference between variant A and B
The only difference is the used LDO. Variant A uses the AS1363, variant B the SPX3819(or pincompatible).

#### Resources:
- AS1363 Datasheet - https://ams.com/eng/content/download/1961/15107/file/AS1364_Datasheet_EN_v3.pdf
- SPX3819 Datasheet - https://www.adafruit.com/datasheets/SPX3819_DS_R202_052014.pdf

- More Pictures V3.1 - http://imgur.com/a/jSkG7 (imgur album)
- More Pictures V3.0 - http://imgur.com/a/w46x3 (imgur album)

#### This adapter on OSH Park:
- ESP8266 Breakout v3.1A - https://oshpark.com/shared_projects/RfAN6raq
- ESP8266 Breakout v3.1B - https://oshpark.com/shared_projects/jsl8ZcFp

#### License
<img src="http://mirrors.creativecommons.org/presskit/buttons/88x31/png/by.png" alt="Creative Commons License - BY" /><br />
Creative Commons Attribution 4.0 International<br />
http://creativecommons.org/licenses/by/4.0/
