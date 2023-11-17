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
|![Skeleton_Sketch_schem.png](./images/Skærmbillede%20fra%202023-11-17%2010-04-44.png))|![Skærmbillede%20fra%202023-11-16%2022-46-32.png](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/images/Skærmbillede%20fra%202023-11-17%2010-37-02.png)|![Olimex-ESP32-PoE_32pins_Sketch_schem.png](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/Olimex-ESP32-PoE_32pins_Sketch_schem.png)|

* Files
  * [skeleton_DIP_8_300mil_schematic.svg](./Skeleton/skeleton_DIP_8_300mil_schematic.svg)
  * [Olimex-ESP32-PoE_32pins_schematic.svg](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/Olimex-ESP32-PoE_32pins_schematic.svg)
  * [Olimex-ESP32-PoE 32pins.fzpz](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/Olimex-ESP32-PoE%2032pins.fzpz)
  * [Olimex-ESP32-PoE_32pins_Sketch_Sketch.fzz](./../Olimex-ESP32-POE/Olimex-ESP32-PoE_32pins/Olimex-ESP32-PoE_32pins_Sketch_Sketch.fzz)

### Pins

By using this name topology, I achieve that Fritzing New Part Editor automatically binds the svg file's leg names together Fritzing leg description

* Somewhere I have read that you should start by counting leg no. from 0 then
  * connector0terminal is connection point for pin 1
  * connector0pin is pin no.1

My pen number schema:

|type|pin|ext1|ext2|uext|batt|
|:---:|:---:|:---|:---|:---|:---|
|rect|1|connector0terminal|connector10terminal|connector20terminal|connector30terminal|
|line|1|connector0pin|connector10pin|connector20pin|connector30pin|
|rect|2|connector1terminal|connector11terminal|connector21terminal|connector31terminal|
|line|2|connector1pin|connector11pin|connector21pin|connector31pin|
|rect|3|connector2terminal|connector12terminal|connector22terminal|connector32terminal|
|line|3|connector2pin|connector12pin|connector22pin|connector32pin|
|rect|4|connector3terminal|connector13terminal|connector23terminal||
|line|4|connector3pin|connector13pin|connector23pin||
|rect|5|connector4terminal|connector14terminal|connector24terminal||
|line|5|connector4pin|connector14pin|connector24pin||
|rect|6|connector5terminal|connector15terminal|connector25terminal||
|line|6|connector5pin|connector15pin|connector25pin||
|rect|7|connector6terminal|connector16terminal|connector26terminal||
|line|7|connector6pin|connector16pin|connector26pin||
|rect|8|connector7terminal|connector17terminal|connector27terminal||
|line|8|connector7pin|connector17pin|connector27pin||
|rect|9|connector8terminal|connector18terminal|connector28terminal||
|line|9|connector8pin|connector18pin|connector28pin||
|rect|10|connector9terminal|connector19terminal|connector29terminal||
|line|10|connector9pin|connector19pin|connector29pin||

