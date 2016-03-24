## V1 - 1117 Adapter
<br />
### Changelog/Updates: <br />
V1.1 - Aug, 2015
- Silkscreen optimizations
- Bottom silkscreen moved from layer bNames to bPlace
- Added lables for bottom header
- Smaller gnd vias (0.02755906)

V1.0 - Jun, 2015
- Initial upload

### Pictures
V1.0 - Bare PCB<br />
<img src="https://github.com/8n1/ESP8266-Breakout-Adapter/blob/master/Breakout%20Adapter%20v1.1%20-%20LM1117/Pictures%20(PCB)/ESP12E%20Breakout%20Adapter%20-%20V1-0.jpeg" width="600" alt="ESP-12 Breakout Adapter V1.0 - Bare PCB" />
<br />
V1.1 - OSH Park renderings<br />
<img src="https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/uploads/project/top_image/9CsYq2PY/i.png" width="300" alt="ESP-12 Breakout Adapter V1.1 - Front" />&nbsp;
<img src="https://644db4de3505c40a0444-327723bce298e3ff5813fb42baeefbaa.ssl.cf1.rackcdn.com/uploads/project/bottom_image/9CsYq2PY/i.png" width="300" alt="ESP-12 Breakout Adapter V1.1 - Back" />
<br />
#### Schematic
<img src="https://raw.githubusercontent.com/8n1/ESP8266-Breakout-Adapter/master/Breakout%20Adapter%20v1.1%20-%20LM1117/ESP12E%20Breakout%20Adapter_sch.png" width="600" alt="ESP-12 Breakout Adapter V1.1 - Schematic" />


### Features
* LM1117 Voltage regulator (or pin compatible)
* Flash and Reset switch
* Pullup resistors for Reset, CH_PD and GPIO0
* Pulldown resistor for GPIO15
* ESP-12E bottom header brougth out (see note)
* Breadboard compatible -> One row on both sides stays free
* Except for the headers and switches, fully SMD

##### Note: The additional bottom header on the ESP-12E can not be used without modifying the ESP module:
http://www.esp8266.com/viewtopic.php?f=32&t=4094

### Partlist
| Part  | Value                      | Info                |
|:------|:---------------------------|:--------------------|
| IC1   | LM1117 or pincompatible    | Voltage regulator |
| C1    | 10µF (Tantal, Case B)      | Input capacitor for IC1 |
| C2    | 10µF (Tantal, Case B)      | Output capacitor for IC1 (see the Datasheet)|
| C3    | 100nF (Ceramic, 0805)      | Decoupling capacitor for the ESP module |
| R1    | 10K (0805) *               | Pullup resistor for CH_PD |
| R2    | 10K (0805) *               | Pulldown resistor for GPIO15 |
| R3    | 10K (0805)                 | Pullup resistor for Reset |
| R4    | 10K (0805)                 | Pullup resistor for GPIO0 |
| SW1   | Tactile switch (THT)       | Flash switch |
| SW2   | Tactile switch (THT)       | Reset switch |

\* **or** 0Ohm resistor/solderbridge if pin is not needed

Pinheader
* 2x 1x8 (2.54mm)
* 2x 1x2 (2.54mm)
* (1x 1x6  (2.54mm))
<br />
Optional "socket" for the esp module
* 2x 1x8 (2mm)
* (1x 1x6 (2mm))


#### Resources:
- LM1117 Datasheet - http://www.ti.com/lit/ds/symlink/lm1117-n.pdf
- AMS1117 Datasheet - http://www.advanced-monolithic.com/pdf/ds1117.pdf

#### This adapter on OSH Park:
- ESP8266 Breakout v1.1 - https://oshpark.com/shared_projects/9CsYq2PY

#### License
<img src="http://mirrors.creativecommons.org/presskit/buttons/88x31/png/by.png" alt="Creative Commons License - BY" /><br />
Creative Commons Attribution 4.0 International<br />
http://creativecommons.org/licenses/by/4.0/
