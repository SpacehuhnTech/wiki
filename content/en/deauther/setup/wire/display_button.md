---
title: "Display, Buttons & LED"
date: 2020-06-10T17:14:05+02:00
weight: 1 # The smaller the higher position in the navigation and vice versa
tags: []
---

### Display

There are 2 types of OLED displays that can be used for this project, the SSD1306 and the SH1106:  

![PICTURE SSD1306 vs SH1106](/media/deauther/ssd1306_sh1106_display.jpg?height=350px)

And they sometimes come with either I2C or SPI:  

![PICTURE I2C vs SPI displays](/media/deauther/i2c_spi_display.jpg?height=380px)

Now for the display it is very important that you know which connection it is using.  
I2C can be connected to any GPIO pin (except 16).  

The SPI however requires following connections:

| Display | GPIO |
| ------- | ---- |
| SCL/CLK/SCK | GPIO 14 (D5) |
| SDA/MOSI | GPIO 13 (D7) |

RST, DC and CS pins can connected to any pin. 

**Best practice is to make a list of all components and their connections!**.

### Buttons
The buttons are pretty simple.  
You need to connect each of them between a gpio pin and GND.  
Like in this Arduino tutorial: https://www.arduino.cc/en/Tutorial/InputPullupSerial

### LED
The LED(s) is completley optional. It's used to give the user a better indication of what the device is currently doing. For example Green = idle, Blue = scanning, RED = deauth attack detected (when scanning).  
You can use single digital LEDs, a RGB LED or a neopixel LED (ws2812).  

By default the LED on GPIO 16 (NodeMCU on-board LED) and the LED on GPIO 2 (ESP-12 and ESP-07 on-module LED) are used. So be sure to disable them if you want to use those pins for something else.  

---

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for deauther/setup/wire/display_button.md&body=I'd like to suggest changes for `deauther/setup/wire/display_button.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki/deauther/setup/wire/display_button)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/setup/wire/display_button.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/setup/wire/display_button.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}