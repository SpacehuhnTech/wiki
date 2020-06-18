---
title: "Esptool"
date: 2020-06-18T14:11:24+02:00
weight: 2 # The smaller the higher position in the navigation and vice versa
tags: []
---
### Esptool
Using the NodeMCU (or any similar development board), the flash location is 0x0000 and the mode is dout.  
`esptool.py -p /dev/ttyUSB0 write_flash -fm dout 0x0000 esp8266_deauther.ino.nodemcu.bin`  
Where `/dev/ttyUSB0` is the COM port of your device, `write_flash` is telling the program to write to flash memory, `-fm dout` is the flash mode and `esp8266_deather.ino.nodemcu.bin` is the name of your .bin file. 

### Esptool-gui
An easy to use GUI flasher for Windows and Mac: [esptool-gui](https://github.com/Rodmg/esptool-gui).  
Select the COM Port and the .bin file (firmware), then just press upload. 

---

{{< footerbuttons >}}