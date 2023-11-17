# Howto make Schematic View Graphics

## Intro

I think you should start your PCB layout by creating a circuit diagram, therefore I will start by creating a Schematic View Graphic, my new component, here I have chosen to start with [Olimex's ESP32-PoE](https://www.olimex.com/Products/IoT/ESP32/ESP32-POE/open-source-hardware).

[Olimex-ESP32-PoE has 4 sets of connectors](https://www.olimex.com/Products/IoT/ESP32/ESP32-POE/resources/ESP32-POE-GPIO.png):  

![](./images/Skærmbillede%20fra%202023-11-15%2022-13-09.png)

* EXT1 & EXT2 each with 10 pins to be connected to my PCB.
* UEXT which is a connector with 10 pins for connecting another device.
* BATT which has 2 pins for connecting a battery

A total of 32 pins to be displayed in my Schematic View Graphics

## Create Schematic View for Olimex-ESP32-PoE from skeleton.svg

|Skeleton_Sketch_schem.png|Olimex-ESP32-PoE_32pins_Sketch_schem.png|Olimex-ESP32-PoE_32pins_Sketch_schem.png|
|:---:|:---:|:---:|
|![Skeleton_Sketch_schem.png](./images/Skærmbillede%20fra%202023-11-17%2010-04-44.png))|![Skærmbillede%20fra%202023-11-16%2022-46-32.png](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/images/Skærmbillede%20fra%202023-11-17%2010-34-01.png)|![Olimex-ESP32-PoE_32pins_Sketch_schem.png](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/Olimex-ESP32-PoE_32pins_Sketch_schem.png)|

* Files
  * [skeleton_DIP_8_300mil_schematic.svg](./Skeleton/skeleton_DIP_8_300mil_schematic.svg)
  * [Olimex-ESP32-PoE_32pins_schematic.svg](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/Olimex-ESP32-PoE_32pins_schematic.svg)
  * [Olimex-ESP32-PoE 32pins.fzpz](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/Olimex-ESP32-PoE%2032pins.fzpz)
  * [Olimex-ESP32-PoE_32pins_Sketch_Sketch.fzz](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/Olimex-ESP32-PoE_32pins_Sketch_Sketch.fzz)

  