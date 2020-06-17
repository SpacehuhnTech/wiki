---
title: "Compiling using Arduino IDE"
date: 2020-06-10T16:41:17+02:00
weight: 2 # The smaller the higher position in the navigation and vice versa
tags: []
---

0) First you have to install and open the [Arduino IDE](https://www.arduino.cc/en/main/software).  

1) In Arduino go to File -> Preferences add *both* URLs in *Additional Boards Manager URLs*  
- `http://arduino.esp8266.com/stable/package_esp8266com_index.json`
- `https://raw.githubusercontent.com/wiki/tobozo/Arduino/package_deauther_index.json` 

(ARM specific package : `https://phpsecu.re/esp8266/arm/package_deauther_index.json`)

![External PICTURE adding board url](https://raw.githubusercontent.com/tobozo/Arduino/deauther/screenshots/board_manager_urls.jpg)

2) Go to Tools -> Board -> Boards Manager, search "esp8266" and install `esp8266` first, then `arduino-esp8266-deauther`  
![External PICTURE installing sdk](https://raw.githubusercontent.com/tobozo/Arduino/deauther/screenshots/board_manager_sdk.jpg)

3) Select your board at Tools -> Board and be sure it is at `ESP8266 Deauther Modules` (and **not** at `ESP8266 Modules`)!  
![External PICTURE select board](https://raw.githubusercontent.com/tobozo/Arduino/deauther/screenshots/screenshot_select_board.jpg)

4) Download the source code for this project from the [releases page](https://github.com/spacehuhn/esp8266_deauther/releases). You can also clone the project to get the latest changes, but you will also get the latest bugs ;)

5) Extract the whole .zip file, navigate to esp8266_deauther and open esp8266_deauther.ino with Arduino.

6) Check your upload settings and press upload!

7) You might want to adjust the display, LED and button configurations. You can do that in the `A_config.h` file (second tab in Arduino). You can also find predefined configfor certain boards there: [A_config.h](https://github.com/SpacehuhnTech/esp8266_deauther/blob/v2/esp8266_deauther/A_config.h#L7).  

---

{{< footerbuttons >}}