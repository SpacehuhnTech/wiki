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

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for deauther/setup/wire/example.md&body=I'd like to suggest changes for `deauther/setup/wire/example.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki/deauther/setup/wire/example)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/main/content/en/deauther/setup/wire/example.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/main/content/en/deauther/setup/wire/example.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}