# Howto make Schematic View Graphics

## Intro

I think you should start your PCB layout by creating a circuit diagram, therefore I will start by creating a Schematic View Graphic, my new component, here I have chosen to start with [Olimex's ESP32-PoE](https://www.olimex.com/Products/IoT/ESP32/ESP32-POE/open-source-hardware).

[Olimex-ESP32-PoE has 4 sets of connectors](https://www.olimex.com/Products/IoT/ESP32/ESP32-POE/resources/ESP32-POE-GPIO.png):  

![](./images/Skærmbillede%20fra%202023-11-15%2022-13-09.png)

* EXT1 & EXT2 each with 10 pins to be connected to my PCB.
* UEXT which is a connector with 10 pins for connecting another device.
* BATT which has 2 pins for connecting a battery

A total of 32 pins to be displayed in my Schematic View Graphics

## Create Schematic View Graphics

|Fritzing SVG file|InkScape Document Properties|
|:---:|:---:|
|![Image from Fritzing](./svg/Olimex-ESP32-PoE_microcontroller_DIP_20_1000mil_1_schematic.svg)|![](./images/Skærmbillede%20fra%202023-11-15%2014-13-32.png)|

* Start Fritzing
  * Select Schematic
    * Parts window select: CORE
      * Under CORE find ICs and select the first one named IC 
        * Drag it into the schematic window
    * In the Inspector window, correct the following
      * Pins from 8 to 32
      * Chip label from IC to CPU
  * Now right-click the new schematic 
    * Select: Edit (New parts editor), the Parts Editor opens
      * Select Schematic
        * Click File -> Show in Folder
          * Find a file with a name like:
          "prefix0000_1675214adb8f7492974344c00e5273a4_1_schematic.svg"
            * Right Clik File and Select: "Open with another program"
            * Select InkScape
            * Check Document Properties: (***Remove Show shadow***)
            * Save file as:
              * Plain SVG (*.svg)
              * Name: "Olimex-ESP32-PoE_microcontroller_DIP_20_1000mil_1_schematic.svg"
* Close Fritzing, ***!!! Do not save***

## Edit Layers and Objects

### Help Group

![Help Group](./images/Skærmbillede%20fra%202023-11-15%2015-13-27.png)

* Create a Help Group
  * Layers and Objects
    * Draw a rectangle
      * Size:
        * X: 0,000 in
        * Y: -0,200 in
        * W: 1,500 in
        * H: 1,500 in
    * Group rectangle
      * Rename Group id: help (***!!! Use XLM Editor***)
      * Rename Rectangle id: background (***!!! Use XLM Editor***)
      * Lower to Botton: Group help
  * Fill and Stroke
    * Fill:
      * RGB: 0,0,012  
      * Stroke paint: No paint
      * Stroke style:
        * Width: 0,000 in
