# meson-sm1-sei610-qca9377-bt

This is a Linux dts/dtb which supports the following hardware on Amlogic TV
S905X3 based boxes such as the X96 Air Q1000 and the X96 Max Plus Q2.

* WiFi
* Gigabit ethernet
* HDMI audio
* Bluetooth

The onboard analogue audio jack is not supported by this dts/dtb.

It has been tested using the Manjaro ARM [linux-aml](https://gitlab.manjaro.org/manjaro-arm/packages/core/linux-aml) 5.12 kernel.

## Compilation

You can build the dtb yourself with `device-tree-compiler`:

```
$ dtc -O dtb -o meson-sm1-sei610-qca9377-bt.dtb meson-sm1-sei610-qca9377-bt.dts
```

# UPDATE 8th JUNE 2022

Bluetooth no longer works using meson-sm1-sei610-qca9377-bt.dtb with Manjaro ARM. I suspect there is an issue with the Manjaro bluez package(s)?

You can get working onboard bluetooth for the X96 Air Q1000 and X96 Max Plus Q2 TV boxes by using the meson-sm1-x96-max-plus-q2.dtb which is now offered as an installation option by the s905X3 builds of [s9xxx Armbian](https://github.com/ophub/amlogic-s9xxx-armbian). Do not use the dtbs in this repo.
