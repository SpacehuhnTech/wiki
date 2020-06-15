---
title: "FAQ"
date: 2020-06-10T17:28:55+02:00
weight: 5 # The smaller the higher position in the navigation and vice versa
tags: []
---

### How to ask a question
I recommend you watch [THIS](https://www.youtube.com/watch?v=53zkBvL4ZB4) video before you post a new issue to ask something.  

### Timeout error
A typical message you get in the web interface is the red `ERROR timeout loading file ...` message.  
Don't worry!  
It tells you that a transmission in the background failed.  
This can happen because: 
- The ESP8266 web server is just randomly unreliable (nothing you can do here, just try again or use the OLED and buttons)
- The WiFi around is very crowded and transmissions are not reliable because of the high traffic (try changing the channel in the settings and restart, or use it in a less crowded area)
- You started an attack and the ESP8266 had to change the channel (you might have to reconnect manually)
- You're scanning for stations (you can reconnect once the scan is finished)
- You're attacking multiple targets and the ESP8266 has to change the WiFi channel constantly (you will have to restart to reconnect)
- The ESP8266 crashed - in this case, please look at [Serial usage](https://github.com/spacehuhn/esp8266_deauther/wiki/Serial) for further debugging.

### Compiler error .irom0.text will not fit in region
An often encoutered error by beginners is `.irom0.text' will not fit in region`.  
This error tells you that the compiled sketch doesn't fit in the flash size you selected.  

Most of the time it's caused by the user selecting 512kb flash size, which is the default size for the generic esp8266 board.  

**So be sure to use the correct [upload settings](https://github.com/spacehuhn/esp8266_deauther/wiki/Installation#upload-settings)**  

Arduino usually prints a very long and unreadable compiler error message, but don't let it confuse you. Most of those are warnings rather than errors.

### How to do a Reset
If you just want to reset the settings you can open a serial connection and type in `reset`.  
The easiest way to do that is using the Arduino Serial monitor. The baudrate is `115200` with `Newline`.  
To erase the Deauther script including the WiFi credentials and everything that is saved in the SPIFFS, use our reset sketch:
https://github.com/spacehuhn/esp8266_deauther/tree/master/Reset_Sketch  
You can either compile and flash the .ino file with Arduino or flash one of the .bin files.  

### 5GHz Support
The ESP8266 supports 2.4GHz WiFi, which is already very impressive if you think about how small, powerful, accessible and affordable this system on a chip is!  
A lot of people are asking for 5GHz support, however **this project is not able to do that**.  
As of right now (2018) no hackable 5GHz SoC is available in the form of something like the ESP8266.  
Even if someone would make such a chip, it would be incompatible with this software.  
You could build a dual band Deauther with a Raspberry Pi and the right WiFi module.  
But as of right now, it's not always easy to find good Dual-Band WiFi chips that support packet injection and monitor mode.

**⚠️ THE ESP8266 DOES NOT AND WILL NOT SUPPORT 5GHZ! ⚠️**

Devices supporting this are more expensive and need special drivers (this will change in the future as new chips are released all the time).
But if you want to try it, look for the `rtl8812au` or `rtl8811au` WiFi modules. Those have already been used to inject packets at 5GHz.  

### ESP32 And ESP8285 Support
ESP32: No  
ESP8285: Yes  
See [Supported Devices](https://github.com/spacehuhn/esp8266_deauther/wiki/Supported-Devices) for more details.  

### Difference between Jammer and Deauther
While a jammer just creates noise on a specific frequency range (i.e. 2.4GHz), a deauthentication attack is only possible due to a vulnerability in the WiFi (802.11) standard. The deauther does not interfer with any frequencies, it is just sending a few WiFi packets that let certain devices disconnect. That enables you to specifically select every target. A jammer just blocks everything within a radius and is therefore highly illegal to use.

Watch this video for a good explanation on the technical and legal differences: 🎬 [WiFi Jammers vs Deauthers | What's The Difference?](https://www.youtube.com/watch?v=6m2vY2HXU60)  

### Why is there no Packet-Monitor/Deauth-Detector in the web interface?
The problem is that you can't have an access point open to host the web server while sniffing WiFi.  
It's like with every other WiFi card. Either you use it as an access point to host a network, as a station to connect to one or you put it in monitor mode to sniff for packets. But you can't have everything at the same time.  

### How to compile .bin files yourself
In Arduino click `Sketch` -> `Export compiled Binary` and a new .bin file will be created in the sketch folder.

### Drivers
If you can't find the COM port of your device, then you probably haven't installed the right drivers yet.
Here are the links to the drivers of the 2 most used UART chips:
- 💾 [CP2102](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers)
- 💾 [CH340](https://sparks.gogo.co.nz/ch340.html)

If you're not sure which chip your board is using, just try both.

### Fix crashes
A crash or exception can have a lot of reasons but before you open a new issue, try this:  
- open a serial connection
- type `reset` to reset all settings
- type `format` to remove all saved files in the on-board file system
- reconnect your device and see if it works now

### Not able to connect to Access Point
There could be a lot of reasons why you can't connect to the ESP8266 with certain devices.  
For example, someone reported that the Intel 7260 WiFi Chip can make problems: https://github.com/spacehuhn/esp8266_deauther/issues/754  
Arduino has example sketches for the ESP8266 to create an access point. You can try that out and see if you can connect to it. If not, then the problem is not related to this project's code and you have to investigate your hardware/software setup further.  

### Removing Deauther
To erase the deauther you can just flash a different sketch. To overwrite the SPIFFS and EEPROM, you can flash our simple [Reset Sketch](https://github.com/spacehuhn/esp8266_deauther/tree/master/Reset_Sketch).  

### espcom error
The `espcom opening` or `espcomm_sync failed` error tells you that your computer couldn't connect to the ESP8266 correctly when trying to upload something.  
Be sure you have the correct COM port selected and use the correct [upload settings](#upload-settings).  
If you can't find the COM port, read [Finding COM Port](#finding-com-port) first.  
Maybe you need to [install the drivers](#drivers).  
Also be sure you use a USB data cable! Sometimes it also helps to restart Arduino or your computer, changing the cable or USB port.  
It was also reported that the Windows-Insider-Program can make problems with the cp2102 drivers.  

If everything else fails, try reflashing the Deauther. See [Removing Deauther](#removing-deauther) and then flash it again.  

### Language doesn't change
If you go to Settings in the web interface, you can change the language. For example `de` is for the German language file.  
To see what languages are supported, have a look at the [lang folder](https://github.com/spacehuhn/esp8266_deauther/tree/master/web_interface/lang) or the description of the latest [release](https://github.com/spacehuhn/esp8266_deauther/releases).  
If the language doesn't change, it is probably because your browser has the old language file cached and doesn't want to reload it. Try deleting your browser cache.  
Or open `192.168.4.1/lang/default.lang` and reload it one or two times.  

### Error writing/saving/reading file
If you get message like `Error saving file` or something similar over serial, there is probably something wrong with the SPIFFS. It happens sometimes that the file system get corrupted for some reason. Usually you can fix it by running the `format` command and then restarting the device.  
If the error persists, please be sure that your [upload settings](https://github.com/spacehuhn/esp8266_deauther/wiki/Installation#upload-settings) are correct, especially the [flash size](https://github.com/spacehuhn/esp8266_deauther/wiki/Installation#flash-size).  

### [AP] request: ... NOT FOUND
This message pops up in the serial command line interface on versions 2.0.0 - 2.0.6.  
In version 2.1.0 it's commented out, due to the big amount of people that reported it as a error.  
It tells you that a file was requested by the client, that couldn't be found in the ESP8266 memory.  
This usually occurs because client devices want to check whether or not the network has a connection to the internet.  

### Attack stops after a while
This is not a bug, it's a feature. To disable it, you have to set the `attackTimeout` setting to `0`.  

---

{{< footerbuttons >}}