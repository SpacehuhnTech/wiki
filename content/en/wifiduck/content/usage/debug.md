---
title: "Debug"
date: 2020-06-07T22:37:27+02:00
weight: 14 # The smaller the higher position in the navigation and vice versa
tags: []
---

To properly debug, you need to have both the Atmega32u4
and the ESP8266 connected via USB to your computer.  

That can be tricky when you only have a all in one board, so it might be useful
you built one yourself. You don't need to solder it, for example you can use an
Arduino Leonardo and a NodeMCU and connect them with jumper cables.  

Now open 2 instances of Arduino (so they run as separate processes!),
select the COM port and open the serial monitor for each device.
You might need to reset the Atmega32u4 to see serial output.
If that causes problems with the i2c connection, try to reset the ESP8266 too. 

---

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for /wifiduck/content/usage/debug.md&body=I'd like to suggest changes for `/wifiduck/content/usage/debug.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki//wifiduck/content/usage/debug)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/master/content/en//wifiduck/content/usage/debug.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/master/content/en//wifiduck/content/usage/debug.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}