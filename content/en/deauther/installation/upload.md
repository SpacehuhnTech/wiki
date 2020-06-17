---
title: "Upload settings"
date: 2020-06-10T16:47:28+02:00
weight: 3 # The smaller the higher position in the navigation and vice versa
tags: []
---

Those are the recommended upload/compile settings for Arduino:
```
Board: Generic ESP8266 Module  
Flash Mode: DOUT
Flash Frequency: 80 MHZ
CPU Frequency: 160 MHz
Flash Size: 1M (256K SPIFFS)
Reset Method: nodemcu
Upload Speed: 115200
Port: <com port of your device>
```
Most NodeMCUs and other development boards have 4MB Flash so you can set the Flash Size to 4M (3M SPIFFS) or select NodeMCU 1.0 as the board.  
A bigger Flash size can give you more memory in the SPIFFS for saving data, scripts or other files. Increasing the SPIFFS can also make it a bit slower, as the ESP8266 has to maintain a bigger file system.  
If you have a board with the ESP-07 (the one with the connector for an external antenna) it probably has only 1MB of flash, so keep the recommended settings above.  
Putting the Upload Speed to 921600 (or other baud rates) gives you a higher upload speed but doesn't always work.  

#### Flash Mode
DOUT should always work. It means Dual Output.  
QIO (quad I/O) uses 4 instead of 2 pins and will make the flash faster. However, you won't be able to use GPIO 9 and 10 (SD2, SD3)! If you flash it with QIO and use those pins, it will crash without a warning.  
More details on the different modes are descripted here: https://github.com/espressif/esptool/wiki/SPI-Flash-Modes

#### Flash Frequency
A higher flash frequency should increase the speed, but it doesn't always work with every module.  
Try out what works the best.  

#### CPU Frequency
We strongly recommend to use 160MHz to get the extra performance out of the chip.  

#### Reset Method
Again, try out what works and use that.  

#### Baud Rate
The recommended baud rate for uploading is 115200. You can try higher baud rates for faster uploading or slower ones if 115200 isn't working very reliable.  

#### Flash Size
The flash size is an important factor!  
![PICTURE different esp8266 modules](/media/deauther/esp_modules.jpg?height=400px)  
The ESP-12 (which is used on most development boards like the NodeMCU) has 4MB of flash memory.  
Other Modules like the ESP-01 and ESP-07 (the one with the antenna connector) come with only 1MB of memory.  
You have to change your upload settings depending on the module you're using.  

For compiling we recommend to use either `1M (256K SPIFFS)` or `4M (3M SPIFFS)`.  
It is also very important to note, that you **must give the SPIFFS some memory**. This software will only work with the SPIFFS enabled, otherwise you will see something like `Initializing SPIFFS...ERROR` on startup.  

---

{{< footerbuttons >}}