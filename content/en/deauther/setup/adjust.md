---
title: "Adjust code"
date: 2020-06-10T17:24:48+02:00
weight: 3 # The smaller the higher position in the navigation and vice versa
tags: []
---

Now that your setup is done, you have to make some changes to the code.  
See [Installation](https://github.com/spacehuhn/esp8266_deauther/wiki/Installation#compiling-using-arduino-ide) on how to compile and upload code using Arduino.  

1) Open Arduino and go to `A_config.h` (second tab)

2) Change all the `#define` settings according to your setup. The default settings are for the [I2C example setup](#example-setup-with-spi-oled), just without the Neopixel LED. Be sure not to confuse the GPIO pins with the NodeMCU pins (D0,D1...)! You can find the NodeMCU pinout above.  

3) Don't forget to change `#define USE_DIPLAY false` to `#define USE_DIPLAY true`

4) Upload your code and test it

5) Save a copy of the `A_config.h` file so it's easy for you to update the software later.

---

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for deauther/setup/adjust.md&body=I'd like to suggest changes for `deauther/setup/adjust.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki/deauther/setup/adjust)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/setup/adjust.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/setup/adjust.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}