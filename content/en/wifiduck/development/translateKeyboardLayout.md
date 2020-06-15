---
title: "Translate Keyboard Layout"
date: 2020-06-07T22:40:43+02:00
weight: 17 # The smaller the higher position in the navigation and vice versa
tags: []
---

Currently the supported keyboard layouts are:  
- [DE](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/locale_de.h)
- [GB](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/locale_gb.h)
- [US](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/locale_us.h)
- [ES](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/locale_es.h)
- [FR (ASCII only)](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/locale_fr.h)

All standard keys are defined in [usb_hid_keys.h](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/usb_hid_keys.h).  
To translate a keyboard layout, you have to match each character on
your keyboard to the one(s) of a US keyboard.  
This stuff is hard to explain in writing and requires a lot of manual work and testing.  

1. Copy one of the existing layouts files, like [locale_us.h](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/locale_us.h).  
Preferably one that is close to your keyboard layout, it will save you time!  
2. Add `#include "locale_xx.h"` to the end of the locales.h file.
3. Rename the file and its variables to your language code.
For example:  
`locale_xx.h` -> `locale_de.h`,  
`ascii_xx` -> `ascii_de`,  
`locale_xx` -> `locale_de`,  
`extended_ascii_xx` -> `extended_ascii_de`,  
`utf8_xx` -> `utf8_de`.  
4. Modify the ASCII array.  
The ASCII array has a fixed size. Each row describes a key.
First a modifier key like `KEY_MOD_LSHIFT`, then a character key.
Some ASCII characters can't be typed or don't require a modifier,
that's where you must place `KEY_NONE`.
Check [usb_hid_keys.h](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/usb_hid_keys.h) for the available keys.  
If multiple modifiers are required, you must use a bitwise OR to connect them: `KEY_MOD_RALT | KEY_MOD_LSHIFT`.  
For example, in [locale_de.h](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/locale_de.h#L136) `Z` is saved as `KEY_MOD_LSHIFT, KEY_Y`.  
This is because German keyboards use QWERTZ instead of the QWERTY layout
and since the letter is uppercase, shift must be pressed as well.   
Thankfully you don't have to trial and error everything, the Hak5 Community
translated a lot of layouts already [here](https://github.com/hak5darren/USB-Rubber-Ducky/tree/master/Encoder/resources). It's just written in a different syntax. For example, `ASCII_20` (20 in hexadecimal) is the 32th character in our ascii array.  
5. Modify or create the extended ASCII array.  
The extended ASCII array doesn't have a fixed size and is only as long as you make it.
First the character code. For example, [ä](https://theasciicode.com.ar/extended-ascii-code/letter-a-umlaut-diaeresis-a-umlaut-lowercase-ascii-code-132.html) has the index 132, or 84 in hex.
It doesn't use a modifier and sits where the apostrophe key is on a US keyboard:
`0x84, KEY_NONE,       KEY_APOSTROPHE, // ä`.  
6. Modify or create the UTF-8 array.  
The UTF-8 array is variable in length, too.  
The first 4 bytes are the character code.  
For example, [Ä](https://www.fileformat.info/info/unicode/char/00c4/index.htm) has the hex code c384 or 0xc3 0x84. The other 2 bytes are not used so we set them to 0.
Because the letter is uppercase, we need to press the shift key and like before, the letter is typed by pressing the same key as the apostrophe key of a US keyboard: `0xc3, 0x84, 0x00, 0x00, KEY_MOD_LSHIFT, KEY_APOSTROPHE, // Ä`.  
7. Edit the hid_locale_t structure.  
If you renamed all variables accordingly, there's nothing left to do.  
8. Go to [duckparser.cpp](https://github.com/spacehuhn/WiFiDuck/blob/master/atmega_duck/duckparser.cpp#L163) at `// LOCALE (-> change keyboard layout)` you can see a bunch of else if statements.
You need to copy one for your layout.  

Before adding GB layout:  
```c
if (compare(w->str, w->len, "US", CASE_SENSETIVE)) {
    keyboard::setLocale(&locale_us);
} else if (compare(w->str, w->len, "DE", CASE_SENSETIVE)) {
    keyboard::setLocale(&locale_de);
}
```

After adding GB layout:
```c
if (compare(w->str, w->len, "US", CASE_SENSETIVE)) {
    keyboard::setLocale(&locale_us);
} else if (compare(w->str, w->len, "DE", CASE_SENSETIVE)) {
    keyboard::setLocale(&locale_de);
} else if (compare(w->str, w->len, "GB", CASE_SENSETIVE)) {
   keyboard::setLocale(&locale_gb);
}
```
9. Test your layout with a Ducky Script that contains all characters of your keyboard. For example:  
```
LOCALE DE
STRING !"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_abcdefghijklmnopqrstuvwxyz{|}~²³äöüÄÖÜß€°§`
ENTER
```
10. Add a link to your layout to [README](README.md), to [web/index.html](web/index.html) and please feel free to improve this tutorial to help future translators!
11. [Create a Pull Request](https://help.github.com/en/articles/creating-a-pull-request)

---

{{< footerbuttons >}}