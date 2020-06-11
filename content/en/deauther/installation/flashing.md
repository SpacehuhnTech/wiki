---
title: "Flashing bin file"
date: 2020-06-10T16:29:54+02:00
weight: 1 # The smaller the higher position in the navigation and vice versa
tags: []
---

## Flashing the firmware bin file
You can find precompiled .bin files on the [release page](https://github.com/spacehuhn/esp8266_deauther/releases). Be sure to download the latest version. The 1 MB file should be good for most devices. If you have a NodeMCU with an ESP-12 you can also use the 4MB file. But all in all, it shouldn't matter that much.  
Use **one** of the following software to flash your ESP8266 with the .bin file.  
If you're beginner, have a look at [Node2Deauther](#node2deauther).  

### Esptool
Using the NodeMCU (or any similar development board), the flash location is 0x0000 and the mode is dout.  
`esptool.py -p /dev/ttyUSB0 write_flash -fm dout 0x0000 esp8266_deauther.ino.nodemcu.bin`  
Where `/dev/ttyUSB0` is the COM port of your device, `write_flash` is telling the program to write to flash memory, `-fm dout` is the flash mode and `esp8266_deather.ino.nodemcu.bin` is the name of your .bin file. 

### Flash Download Tools
Espressif has an official GUI tool for Windows.  
It has a lot of options and can be used for the ESP8266, ESP8285 and ESP32.  
You can find it on Espressif's download page here: https://www.espressif.com/en/support/download/other-tools  
(if the link changed, just search for `esp flash download tool`)  

### Node2Deauther
![Node2Deauther Screenshot](https://raw.githubusercontent.com/mrvodka007/n2d/master/Preview-IMG/ScreenShot1.PNG)  
[mrvodka007](https://github.com/mrvodka007) created this user friendly all-in-one flasher tool.  
It helps you go through the process step by step and also provides the drivers you'll need.  
[https://github.com/mrvodka007/n2d](https://github.com/mrvodka007/n2d)

### Esptool-gui
An easy to use GUI flasher for Windows and Mac: [esptool-gui](https://github.com/Rodmg/esptool-gui).  
Select the COM Port and the .bin file (firmware), then just press upload.  

### NodeMCU-flasher
Another easy to use GUI flasher, but this time only for Windows: [nodemcu-flasher](https://github.com/nodemcu/nodemcu-flasher).  
Select the COM port, go to config and select your .bin file at *0x000000*.   
Go back to Operation and click Flash.  
![Recommended Flash settings NodeMCU Flasher](/media/deauther/flash_settings_nodemcu_flasher.jpg?height=400px)  

⚠️ The NodeMCU Flasher is outdated and can be buggy. If it doesn't work, just try flashing it again and see the [Installation tips and tricks](#installation-tips-and-tricks).  

---

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for deauther/installation/flashing.md&body=I'd like to suggest changes for `deauther/installation/flashing.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki/deauther/installation/flashing)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/installation/flashing.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/installation/flashing.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}