---
title: "FAQ"
date: 2020-06-07T22:38:02+02:00
weight: 15 # The smaller the higher position in the navigation and vice versa
tags: []
---

{{% collapsible "What's new compared to the WiFi Ducky?" %}}
Changes since the [WiFi Ducky](https://github.com/spacehuhn/wifi_ducky/) predecessor include:
* Support for multiple keyboard layouts
* No size limit per script (other than the physical memory limit)
* No line length limit for the `STRING` command
* Faster typing speed
* Optional Neopixel or Dotstar LED
* Entirely new web interface
* Support for I2C to enable easier debugging and DIY builds
{{% /collapsible %}}

{{% collapsible "I forgot the password" %}}
Flash the ESP8266 again, but make sure that you select `Erase Flash: Sketch + WiFi Settings`
under Tools in the Arduino IDE. 
{{% /collapsible %}}

{{% collapsible "Does this work on an ATTINY85 or DIGISPARK too?" %}}
Because of the limited resources, DIGISPARK or other ATTINY85 based development boards are **NOT supported!**  
{{% /collapsible %}}

{{% collapsible "I still have a question, where can I ask?" %}}
If you have a question, you can check out the [issue section](https://github.com/spacehuhn/WiFiDuck/issues).  
Use the search function to look up similar questions, be sure to check both open and closed issues!  
{{< youtube 53zkBvL4ZB4 >}}
{{% /collapsible %}}

---

{{< footerbuttons >}}