---
title: "Usage"
date: 2020-06-10T17:27:20+02:00
weight: 4 # The smaller the higher position in the navigation and vice versa
tags: []
---

Once you succeed into flashing the ESP8266, you are ready to go ahead and use it.  
Now there are different ways of using the Deauther.  

# 📳 Web interface
That is the go-to for most users, but it has some downsides. For example you can't expect to have a perfect connection to the web interface while you are scanning or attacking.
More on how to use the web interface is explained [here](https://github.com/spacehuhn/esp8266_deauther/wiki/Web).

# 🎦 OLED Display
The Deauther comes with a built-in support for the small OLEDs you can find on eBay or AliExpress.
It's nice if you want to have something headless. It can do most of the stuff the web interface can. One big advantage over the web interface is the [PacketMonitor](https://github.com/spacehuhn/PacketMonitor) with the [DeauthDetector](https://github.com/spacehuhn/DeauthDetector) built-in.
See [Setup Display & Buttons](https://github.com/spacehuhn/esp8266_deauther/wiki/Setup-Display-&-Buttons) on how to connect and adjust everything.
Click [here](https://github.com/spacehuhn/esp8266_deauther/wiki/Display) for more information about how to use it.

# 🔡 Serial
The biggest new feature of version 2.0 is the command line interface over serial.
You can control most functions with it and you can also write scripts for it.
More on how to use it [here](https://github.com/spacehuhn/esp8266_deauther/wiki/Serial).
All serial commands are listed in the [serialcommands.md](https://github.com/spacehuhn/esp8266_deauther/blob/master/serialcommands.md) file.

---

{{< wikibuttons >}}