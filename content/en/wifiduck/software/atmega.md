---
title: "Flash Atmega32u4"
date: 2020-06-17T21:06:41+02:00
weight: 2 # The smaller the higher position in the navigation and vice versa
tags: []
pre: "<b>2.</b>&nbsp;"
---

1. Open `atmegaduck/atmega_duck.ino` with the Arduino IDE.
2. Under `Tools` > `Board` in the `WiFi Duck AVR` section, select your board;
for example, `Sparkfun Pro Micro`.
3. Connect the Atmega32u4 board via USB and select its port under `Tools` > `Port`.
4. [Optional] Under `Tools` you can enable the LED and set its pin.
You can also change the USB ID to make it appear as a certain type of keyboard.
5. Press Upload.


**Unbrick Atmega32u4**

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

{{< footerbuttons >}}