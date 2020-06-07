---
title: "Flash Software"
date: 2020-06-07T22:27:27+02:00
weight: 10 # The smaller the higher position in the navigation and vice versa
tags: []
---

[Video Tutorial](https://youtu.be/VQAzxBefLZo) 

### Preparations

1. Download and install the [Arduino IDE](https://www.arduino.cc/en/main/software).
2. Start the Arduino IDE, go to `File` > `Preferences`.
3. At *Additional Board Manager ULRs* enter `https://raw.githubusercontent.com/spacehuhn/hardware/master/wifiduck/package_wifiduck_index.json`. You can add multiple URLs, separating them with commas.
4. Go to `Tools` > `Board` > `Board Manager`, search for `wifi duck` and install `WiFi Duck AVR Boards` and `WiFi Duck ESP8266 Boards`.
5. [Download](https://github.com/spacehuhn/WiFiDuck/archive/master.zip) and extract this repository or [git clone](https://github.com/spacehuhn/WiFiDuck.git) it.

If you can't find the COM port of ESP8266 board, then you're probably missing the right drivers.
Here are links to drivers of the 2 most used UART chips on ESP8266 development boards:
- 💾 [CP2102](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers)
- 💾 [CH340](https://sparks.gogo.co.nz/ch340.html)

### Flash Atmega32u4

1. Open `atmegaduck/atmega_duck.ino` with the Arduino IDE.
2. Under `Tools` > `Board` in the `WiFi Duck AVR` section, select your board;
for example, `Sparkfun Pro Micro`.
3. Connect the Atmega32u4 board via USB and select its port under `Tools` > `Port`.
4. [Optional] Under `Tools` you can enable the LED and set its pin.
You can also change the USB ID to make it appear as a certain type of keyboard.
5. Press Upload.

### Flash ESP8266

1. Open `esp_duck/esp_duck.ino` with the Arduino IDE.
2. Under `Tools` > `Board` in the `WiFi Duck ESP8266` section, select your board.
For example `NodeMCU 1.0 (ESP-12E Module)`.
3. Connect the ESP8266 board via USB and select its port under `Tools` > `Port`.
5. Press Upload.

**Pro Tip:** If the ESP8266 is already running this software
and you just want to update it, you don't have to connect it via USB.
You can update it over the air! Simply connect to the Wi-Fi network its hosting
(default SSID and password is `wifiduck`).  
In Arduino under `Tools` > `Port` you should now see a network port.
Select it and press `Upload`.  

**Note:** It can take a minute until the device is ready.
After the initial flashing, the ESP8266 has to format its memory.  

If you connected the RGB LED:
* Blue LED = Connection working
* Green LED = Device ready

### Unbrick Atmega32u4

If you flashed your Atmega32u4 board with the wrong bootloader,
it will no longer appear in the port selection after you connect it.  
To solve this, you need to:

1. Connect the reset pin `RST` to ground `GND`.
Preferably with a jumper wires, because you need to be able to disconnect it quickly.  
2. Open a sketch, `atmegaduck/atmega_duck.ino` or an empty sketch.  
**Make sure to have the correct board selected under `Tools` > `Board`!**
3. Connect the board with the wire still connected.
4. Press `Upload` and as soon as you see `Compiling...` turn to `Uploading...`, disconnect the wire.  

Now it should flash the sketch and the correct bootloader.  

---

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for /wifiduck/content/flashSoftware.md&body=I'd like to suggest changes for `/wifiduck/content/flashSoftware.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki//wifiduck/content/flashSoftware)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/master/content/en//wifiduck/content/flashSoftware.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/master/content/en//wifiduck/content/flashSoftware.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}