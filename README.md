# meson-sm1-sei610-qca9377-bt

This is a Linux dts/dtb which supports the following hardware on Amlogic TV
S905X3 based boxes such as the X96 Air Q1000 and the X96 Max Plus Q2.

* WiFi
* Gigabit ethernet
* HDMI audio
* Bluetooth

The onboard analogue audio jack is not supported by this dts/dtb.

It has been tested using the Manjaro ARM [linux-aml](https://gitlab.manjaro.org/manjaro-arm/packages/core/linux-aml) 5.12 kernel.

UPDATE JUNE 2022

Bluetooth no longer works using meson-sm1-sei610-qca9377-bt.dtb with Manjaro ARM.

You can get working onboard bluetooth on the X96 Air Q1000 and X96 Max Plus Q2 by using meson-g12a-x96-max-plus-q2.dtb with a 5.15.x+ kernel running under [s9xxx Armbian](https://github.com/ophub/amlogic-s9xxx-armbian). This dtb has most recently been tested with the Linux 5.15.45-flippy-73 kernel.

meson-g12a-x96-max-plus-q2.dtb doesn't have working onboard ethernet under the Armbian 5.10.x kernels but WiFi and bluetooth both work under Linux 5.10.120-flippy.

## Compilation

You can build the dtb yourself with `device-tree-compiler`:

```
$ dtc -O dtb -o meson-sm1-sei610-qca9377-bt.dtb meson-sm1-sei610-qca9377-bt.dts
```
