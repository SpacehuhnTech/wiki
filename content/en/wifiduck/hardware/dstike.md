---
title: "DSTIKE WiFi Duck"
date: 2020-06-07T22:26:16+02:00
weight: 5 # The smaller the higher position in the navigation and vice versa
tags: []
---

![DSTIKE WiFi Duck](/media/wifi_duck/dstikeboard.jpg?height=200px)  

If you like to support this project,
Travis Lin sells a custom designed development board which comes preflashed with this software!  

You can purchase it here:  
- [tindie](https://www.tindie.com/products/lspoplove/dstike-wifi-duck/)
- [DSTIKE](https://dstike.com/products/dstike-wifi-duck)
- [AliExpress](https://www.aliexpress.com/item/4000256143274.html)

You can update the ESP8266 over the air and flash the Atmega32u4 via Arduino,
all while enclosed in its neat little case.  

{{< youtube e3-nsOjclsY >}}

If you wish to develop your own software or help improve this one,
the 8-bit DIP-switch makes it easy for you to access the Atmega32u4 or ESP8266 independently.  

To flash it see [Flash Software](#flash-software).
Or select `Arduino Leonardo` for the Atmega32u4
and `NodeMCU 1.0 (ESP-12E Module)` for the ESP8266.  

| Mode | Atmega32u4 | ESP8266 | DIP-switch | Image |
| --- | --- | --- | --- | --- |
| Default Operating Mode | USB | On | 10101101 | ![dstike wifi duck work mode](/media/wifi_duck/dstike_normal.jpg?height=50px) |
| Atmega32u4 Flash Mode | USB | Off |10101010 | ![dstike wifi duck atmega mode](/media/wifi_duck/dstike_atmega.jpg?height=50px) |
| ESP8266 Flash Mode | Off | USB | 01011101 | ![dstike wifi duck esp8266 mode](/media/wifi_duck/dstike_esp8266.jpg?height=50px) |

---

{{< footerbuttons >}}