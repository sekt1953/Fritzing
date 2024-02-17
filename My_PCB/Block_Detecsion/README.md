# Block Detector

## Prototype I2C IO_Interface

|Breadbord|Schematic|
|:---:|:---:|
|![Breadbord](./Images/I2C_%20IO_Interface_proto_bb.png)|![Schematic](./Images/I2C_%20IO_Interface_proto_schem.png)

* Fritzing files:
  * [I2C_IO_Interface_proto.fzz](./I2C_%20IO_Interface_proto.fzz)

## I2C IO_Interface PCB

|PCB|Schematic|
|:---:|:---:|
|![PCB](./Images/I2C_%20IO_Interface_pcb.png)|![Schematic](./Images/I2C_%20IO_Interface_schem.png)

* Fritzing files:
  * [I2C_IO_Interface.fzz](./I2C_%20IO_Interface.fzz)

## BlockDetector  Width 6 Dioder and Optokobler

**BlockDetectormed_6_Dioder_Optokobler card** send it data to **I2C IO_Interface card** that then send data via [ESPHome I2C BUS](https://esphome.io/components/i2c.html) to [Home Assistant](https://www.home-assistant.io/), that then handle the data.

|PCB|Schematic|
|:---:|:---:|
|![PCB](./Images/BlockDetectormed_6_Dioder_Optokobler_pcb.png)|![Schematic](./Images/BlockDetectormed_6_Dioder_Optokobler_schem.png)

* Fritzing files:
  * [BlockDetectormed_6_Dioder_Optokobler.fzz](./BlockDetectormed_6_Dioder_Optokobler.fzz)
