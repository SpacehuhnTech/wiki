---
title: "Flashing"
date: 2020-06-18T14:10:47+02:00
weight: 2 # The smaller the higher position in the navigation and vice versa
tags: []
---
### Flash Download Tools
Espressif has an official GUI tool for Windows.  
It has a lot of options and can be used for the ESP8266, ESP8285 and ESP32.  
You can find it on Espressif's download page here: https://www.espressif.com/en/support/download/other-tools  
(if the link changed, just search for `esp flash download tool`)  

### Flashing the firmware bin file
You can find precompiled .bin files on the [release page](https://github.com/spacehuhn/esp8266_deauther/releases). Be sure to download the latest version. The 1 MB file should be good for most devices. If you have a NodeMCU with an ESP-12 you can also use the 4MB file. But all in all, it shouldn't matter that much.  
Use **one** of the following software to flash your ESP8266 with the .bin file.  
If you're beginner, have a look at [Node2Deauther](#node2deauther).  

#### {{% children depth="2" %}}

---

{{< footerbuttons >}}