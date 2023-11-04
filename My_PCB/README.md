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

|||
|:---:|:---:|
|![schem](./PWM_Light_Controller/PWM_Light_Controler_v1_3/PWM_Light_Controler_v1_3_schem.png)|![pcb](./PWM_Light_Controller/PWM_Light_Controler_v1_3/PWM_Light_Controler_v1_3_pcb.png)||

## PCB Board for modelrailway

WM_Light_Controller:  
The PWM Light Controller is a light controller based on an ESP32 and Power Mosfet, it also has an I2C interface where I have connected a BMP230 climate sensor.

### [occupied_sensor](./occupied_sensor/) 

|||
|:---:|:---:|
|![schem](./occupied_sensor/v1/occupied_sensor_schem.png)|![](./occupied_sensor/v1/png/occupied_sensor_pcb.png)||

Occupied Sensor:  
Is a card to detect if there are trains on a track section, be it wagons or locomotives, the printed card has 64 inputs.

### [Darlinton_Relay_and_Led_Driver](./Darlinton_Relay_and_Led_Driver/)

|||
|:---:|:---:|
|![schem](./Darlinton_Relay_and_Led_Driver/png/PCF8574_ULN2803_schem.png)|![pcb](./Darlinton_Relay_and_Led_Driver/png/PCF8574_ULN2803_pcb.png)

Darlinton_Relay_and_Led_Driver:  
The printed circuit board is a driver card for leds and relays with an anode (+power).