---
title: "Examples"
date: 2020-06-10T17:17:28+02:00
weight: 2 # The smaller the higher position in the navigation and vice versa
tags: []
---

### Example setup with I2C OLED

| Display | GPIO |
| ------- | ---- |
| GND | GND |
| VCC/VDD | VCC / 3.3V |
| SCL/CLK/SCK | GPIO 4 (D2) |
| SDA | GPIO 5 (D1) |

| Button | GPIO |
| ------ | ---- |
| UP | GPIO 14 (D5) |
| Down | GPIO 12 (D6) |
| A | GPIO 13 (D7) |

| NEOPIXEL LED | GPIO |
| ------ | ---- |
| GND | GND |
| VCC | VCC/3.3V |
| DIN | GPIO 9 (SD2) |

![PICTURE i2c build](/media/deauther/example_built_i2c.jpg?height=400px)

### Example setup with SPI OLED

| Display | GPIO |
| ------- | ---- |
| GND | GND |
| VCC/VDD | VCC / 3.3V |
| SCL/CLK/SCK | GPIO 14 (D5) |
| SDA/MOSI | GPIO 13 (D7) |
| RST/RES/RESET | GPIO 5 (D1) |
| DC | GPIO 4 (D2) |
| CS | GPIO 15 (D8) **or** GND |

| Button | GPIO |
| ------ | ---- |
| UP | GPIO 0 (D3) |
| Down | GPIO 12 (D6) |
| A | GPIO 2 (D4) |

| NEOPIXEL LED | GPIO |
| ------ | ---- |
| GND | GND |
| VCC | VCC/3.3V |
| DIN | GPIO 9 (SD2) |

![PICTURE spi build](/media/deauther/example_built_spi.jpg?height=400px)

---

{{< footerbuttons >}}