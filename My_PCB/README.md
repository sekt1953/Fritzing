# My PCB maked with Fritzing

I'm quite happy with using Fritzing to make my printed circuit boards, it can do most of what I need.

## List

* PCB for Home Assistant
  * [PWM_Light_Controller](./PWM_Light_Controller/PWM_Light_Controler_v1_3/PWM_Light_Controler_v1_3.fzz)
* PCB for Modelrailway
  * [occupied_sensor](./occupied_sensor/)
  * [Darlinton_Relay_and_Led_Driver](./Darlinton_Relay_and_Led_Driver/)

## PCB Board for Home Assistant

### [PWM_Light_Controller](./PWM_Light_Controller/PWM_Light_Controler_v1_3/PWM_Light_Controler_v1_3.fzz)

The PWM Light Controller is a light controller based on an ESP32 and Power Mosfet, it also has an I2C interface where I have connected a BMP230 climate sensor.

|Schematic|PCB|
|:---:|:---:|
|![schem](./PWM_Light_Controller/PWM_Light_Controler_v1_3/PWM_Light_Controler_v1_3_schem.png)|![pcb](./PWM_Light_Controller/PWM_Light_Controler_v1_3/PWM_Light_Controler_v1_3_pcb.png)||

* [Fritzing file for download:](./PWM_Light_Controller/PWM_Light_Controler_v1_3/PWM_Light_Controler_v1_3.fzz)

<hr>

## PCB Board for modelrailway

### [occupied_sensor](./occupied_sensor/) work in progress

Is a card to detect if there are trains on a track section, be it wagons or locomotives, the printed card has 64 inputs.

|Schematic|
|:---:|
|![schem](./occupied_sensor/v1/occupied_sensor_schem.png)|

|copper_top|copper_bottom|silk_top|
|:---:|:---:|:---:|
|![copper_top](./occupied_sensor/v1/svg/occupied_sensor_etch_copper_top.svg)|![copper_bottom](./occupied_sensor/v1/svg/occupied_sensor_etch_copper_bottom.svg)|![silk_top](./occupied_sensor/v1/svg/occupied_sensor_etch_silk_top.svg)|

* [Fritzing file for download:](./occupied_sensor/v1/occupied_sensor.fzz)

## LedDriver with optocoupler

### V6.1

The Led Driver printed circuit board is made with optocouplers in order to realize that many LEDs are already mounted with a common cathode, and therefore cannot be controlled with a darlington array, which needs the LEDs to be mounted with a common anode.

|Schematic|
|:---:|
|![schem](./LedDriver/v6.1/png/Skærmbillede%20fra%202023-11-05%2021-52-42.png)|

||PCB|
|:---|:---|
|copper_top|![copper_top](./LedDriver/v6.1/svg/PCB-LedDriver-V6.1_etch_copper_top.svg)|
|copper_bottom|![copper_bottom](./LedDriver/v6.1/svg/PCB-LedDriver-V6.1_etch_copper_bottom.svg)|
|silk_top|![silk_top](./LedDriver/v6.1/svg/PCB-LedDriver-V6.1_etch_silk_top.svg)|

* [Fritzing file for download:](./LedDriver/v6.1/PCB-LedDriver-V6.1.fzz)

### Error i version 6.1 fix in 6.4

|Error v6.1|Fix v6.4|
|:---|:---|
|![Error](./LedDriver/v6.1/png/PCB-Error-V6.1_schem.png)|![Fix](./LedDriver/v6.1/png/PCB-Fix-V6.4_schem.png)
|See the blue marking|See marking|

### V6.4 work in progress

v6.4 fixes the plug bug of v6.1 and implements reverse current protection.

![reverse](./LedDriver/ReverseProtection/Reverseprotection%20_schem.png)

|Schematic|
|:---:|
|![schem](./LedDriver/v6.4/png/PCB-LedDriver-V6.4_schem.png)|

||PCB|
|:---|:---|
|copper_top|![copper_top](./LedDriver/v6.4/svg/PCB-LedDriver-V6.4_etch_copper_top.svg)|
|copper_bottom|![copper_bottom](./LedDriver/v6.4/svg/PCB-LedDriver-V6.4_etch_copper_bottom.svg)|
|silk_top|![silk_top](./LedDriver/v6.4/svg/PCB-LedDriver-V6.4_etch_silk_top.svg)|

* [Fritzing file for download:](./LedDriver/v6.4/PCB-LedDriver-V6.4.fzz)

## [LedDriver with Darlinton array](./Darlinton_Relay_and_Led_Driver/) work in progress

The printed circuit board is a driver card for leds and relays with an common Anode (+power).

|Schematic|
|:---:|
|![schem](./Darlinton_Relay_and_Led_Driver/png/PCF8574_ULN2803_schem.png)|

|copper_top|copper_bottom|silk_top|
|:---:|:---:|:---:|
|![copper_top](./Darlinton_Relay_and_Led_Driver/svg/PCF8574_ULN2803_etch_copper_top.svg)|![copper_bottom](./Darlinton_Relay_and_Led_Driver/svg/PCF8574_ULN2803_etch_copper_bottom.svg)|![silk_top](./Darlinton_Relay_and_Led_Driver/svg/PCF8574_ULN2803_etch_silk_top.svg)|

* [Fritzing file for download:](./Darlinton_Relay_and_Led_Driver/PCF8574_ULN2803.fzz)