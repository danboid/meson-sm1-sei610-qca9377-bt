# meson-sm1-sei610-qca9377-bt

This is a Linux dts/dtb which supports the following hardware on Amlogic TV
S905X3 based boxes such as the X96 Air Q1000:

* WiFi
* Gigabit ethernet
* HDMI audio
* Bluetooth

The onboard audio of the X96 Air is not supported by this dts.

It has been tested using the Manjaro ARM [linux-aml](https://gitlab.manjaro.org/manjaro-arm/packages/core/linux-aml) 5.12 kernel. 

## Compilation

You can build the dtb yourself with `device-tree-compiler`:

```
$ dtc -O dtb -o meson-sm1-sei610-qca9377-bt.dtb meson-sm1-sei610-qca9377-bt.dts
```
