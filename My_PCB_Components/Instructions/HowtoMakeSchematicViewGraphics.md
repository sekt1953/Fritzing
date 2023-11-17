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

#### Pin_id Schema

|type|pin|ext1|ext2|uext|batt|
|:---:|---:|:---|:---|:---|:---|
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

### Pin_label text Schema

* [ESP32-POE latest schematic in PDF format](https://github.com/OLIMEX/ESP32-POE/blob/master/HARDWARE/ESP32-PoE-hardware-revision-K/ESP32-PoE_Rev_K.pdf)
* [ESP32-POE GPIO map](https://www.olimex.com/Products/IoT/ESP32/ESP32-POE/resources/ESP32-POE-GPIO.png)

|nr.|ext1|nr.|ext2|nr.|uext|nr.|batt|
|---:|:---|:---|:---|:---|:---|:---|:---|
|1|+5V IN/Out|11|GPI39|21|+3V3 Out|31|+BATT|
|2|+3V3 Out|12|GPI36\RXD|22|GND|32|-BATT|
|3|GND|13|GPI35|23|GPIO4\TXD||
|4|EN|14|GPI34|24|GPI36\RXD||
|5|GPIO0|15|GPIO33\HSCLK|25|GPIO16\SCL||
|6|GPIO1|16|GPIO32\HSCMD|26|GPIO13\SDA||
|7|GPIO2\HSDATA|17|GPIO16\SCL|27|GPIO15\HSCMD||
|8|GPIO3|18|GPIO15|28|GPIO2\HSDATA||
|9|GPIO4\TXD|19|GPIO14|29|GPIO14\HSCLK||
|10|GPIO5\SPICS|20|GPIO13\SDA|30|GPIO5\SPICS||

## How I make it

### Create new file:

* Copy the "[skeleton_DIP_8_300mil_schematic.svg](./Skeleton/skeleton_DIP_8_300mil_schematic.svg)" to working directory
* Rename the skeleton to "Olimex-ESP-PoE_32_schematic.svg" or whatever name you want to use for your component

### Set the size of your component:

* Set "background" size
  * Select "Object -> Layers and Objects"
  * Expand the help group
    * Select "background" rectangle object
    * Select "Edit -> XML Editor"
    * Check and edit settings to:
      * |Name|Value|
        |:---|:---|
        |id|background|
        |width|1500|
        |height|1700|
        |x|0|
        |y|0|
        |fill|none|
        |fill-opacity|0.15|
        |stroke|none|
        |stroke-width|0|
        |stroke-dasharray|none|
      * !!! Note: Do not used "Object -> File And Stroke" it will create a style-object, if there is any style-object then delete it.
    * Resize to content:
      * Select: "File -> Document Properties"
      * Click: "Display -> Front page -> Resize to content"
    * Remove Shadow:
      * UnCheck "Display -> Display -> show shadow"
* Set "part_symbol" size:
  * Select "Object -> Layers and Objects"
  * Expand the schematic group
    * Select "part_symbol" rectangle object
    * Select "Edit -> XML Editor"
    * Check and edit settings to:
      * |Name|Value|
        |:---|:---|
        |id|part_symbol|
        |width|1300|
        |height|1500|
        |x|100|
        |y|100|
        |fill|none|
        |stroke|#000000|
        |stroke-width|12|
        |stroke-linecap|round|
        |stroke-dasharray|none|
        |stroke-opacity|1|
      * !!! Note: Do not used "Object -> File And Stroke" it will create a style-object, if there is any style-object then delete it.
* |Before||Now|
  |:---|:---|:---|
  |![](./demo/images/Skærmbillede%20fra%202023-11-17%2014-35-45.png)|![](./demo/images/Skærmbillede%20fra%202023-11-17%2014-36-12.png)|![](./demo/images/Skærmbillede%20fra%202023-11-17%2014-37-19.png)|

### Edit schematic group names

* Select "Layers and Object"
  * Expand "pin_numbers" group
  * Rename "pin_numbers" groups:
    * |Old|New|
      |:---|:---|
      | pin_numbers_west|pin_numbers_ext1|
      | pin_numbers_south|pin_numbers_batt|
      | pin_numbers_east|pin_numbers_ext2|
      | pin_numbers_north|pin_numbers_uext|
  * Expand "pin_labels" group
  * Rename "pin_labels" groups:
    * |Old|New|
      |:---|:---|
      | pin_labels_west|pin_labels_ext1|
      | pin_labels_south|pin_labels_batt|
      | pin_labels_east|pin_labels_ext2|
      | pin_labels_north|pin_labels_uext|
  * Expand "pins" group
  * Rename "pins" groups:
    * |Old|New|
      |:---|:---|
      | pins_west|pins_ext1|
      | pins_south|pins_batt|
      | pins_east|pins_ext2|
      | pins_north|pins_uext|
* |Before||Now||
  |:---|:---|:---|:---|
  |![before L&O](./demo/images/Skærmbillede%20fra%202023-11-17%2014-03-41.png)|![before XML](./demo/images/Skærmbillede%20fra%202023-11-17%2014-09-27.png)|![now L&O](./demo/images/Skærmbillede%20fra%202023-11-17%2014-16-51.png)|![now xml](./demo/images/Skærmbillede%20fra%202023-11-17%2014-16-25.png)

### Duplicate Pins

* Select Layers and Object -> schematic -> pins -> pins_ext1
  * Select Objects "connector0terminal" to "connector1pin"
    * Press {[CTRL]+D to Duplicate Pins
    * Move Pens to position by "X: or Y: - or +" sign in top of frame
    * Repeate the duplication until there are 10 pens.
  * Select XML Editor
    * Rename pins following the "Pen_id Schema" listed in top
* Repeate this process for all "pins" groups.
* |Before|Now|
  |:---|:---|
  |![before](./demo/images/Skærmbillede%20fra%202023-11-17%2014-43-55.png)|![after](./demo/images/Skærmbillede%20fra%202023-11-17%2014-46-58.png)|
  |![](./demo/images/Skærmbillede%20fra%202023-11-17%2015-04-12.png)|![](./demo/images/Skærmbillede%20fra%202023-11-17%2015-18-40.png)

### Duplicate Pin Labels

* Select Layers and Object -> schematic -> labels -> pin_labels_ext1
  * Select Objects "label0" & "label1"
    * Press {[CTRL]+D to Duplicate Pins
    * Move Pens to position by "X: or Y: - or +" sign in top of frame
    * Repeate the duplication until there are 10 pens.
  * Select XML Editor
    * Rename pins following the "Pin_label Schema" listed in top
* Repeate this process for all "pins_labes" groups.
* |Before|Now|
  |:---|:---|
  |![](./demo/images/Skærmbillede%20fra%202023-11-17%2015-33-47.png)|![](./demo/images/Skærmbillede%20fra%202023-11-17%2016-00-00.png)

### Duplicate Pin Numbers

* Select Layers and Object -> schematic -> labels -> pin_numbers_ext1
  * Objects "text0" & "text1"
    * Press {[CTRL]+D to Duplicate Pins
    * Move Pens to position by "X: or Y: - or +" sign in top of frame
    * Repeate the duplication until there are 10 pens.
  * Select XML Editor
    * Rename pins following the "Pin_label Schema" listed in top
* Repeate this process for all "pin_numbers" groups.
* |Before|Now|
  |:---|:---|
  |![](./demo/images/Skærmbillede%20fra%202023-11-17%2016-17-46.png)|![](./demo/images/Skærmbillede%20fra%202023-11-17%2016-26-06.png)
