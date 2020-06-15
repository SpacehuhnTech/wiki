---
title: "Tools"
date: 2020-06-10T16:59:36+02:00
weight: 1 # The smaller the higher position in the navigation and vice versa
tags: []
---

### Before you continue
Using the display interface is completely optional.  
The ESP8266 Deauther can also just be used over serial or the web interface.  

You should know some basics of how to use, code and create stuff with Arduino.  
If you don't, then we highly recommend you to get some sort of Arduino starter kit and start learning. The steps of this tutorial are very simple, but if you have never done something like this, it's very important to get a basic knowledge about the topic first!  

I will focus on the NodeMCU in this tutorial since it is the most popular ESP8266 based development board. Every other development board using the ESP8266 should work just like that.  

### What you need
- a breadboard
- jumper wires
- an ESP8266 dev board (i.e. NodeMCU)
- 3 - 6 buttons (3 required, optional up to 6)
- a SSD1306 or SH1106 OLED display with 128x64 pixels
- optional: a RGB LED (3 single LEDs or a neopixel will also work)
- optional but recommended: 2x 10k ohm resistors
- a working Arduino setup that can compile this project (see [Installation](https://github.com/spacehuhn/esp8266_deauther/wiki/Installation) )
- patience
- common sense
- the ability to read and follow this tutorial carefully
- also recommended: know how to read error messages and use google correctly

For a beginner it's recommended to only use 3 buttons (you can add more later), ab i2c display (those with 4 pins) and (optional) a neopixel as RGB LED.  

**You can find links to everything you need for this [here](https://github.com/PwnKitteh/InsanelyCheapElectronics#deauther-20).**

---

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for deauther/setup/need.md&body=I'd like to suggest changes for `deauther/setup/need.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki/deauther/setup/need)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/main/content/en/deauther/setup/need.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/main/content/en/deauther/setup/need.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}