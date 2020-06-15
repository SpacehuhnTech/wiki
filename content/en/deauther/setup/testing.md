---
title: "Testing"
date: 2020-06-10T17:26:07+02:00
weight: 4 # The smaller the higher position in the navigation and vice versa
tags: []
---

Now when everything is correctly setup and uploaded, you have to open the serial monitor with arduino.  
Make sure to set the baud rate to 115200 and select `Newline`.  
If you see that the device is resetting every few seconds, check the code! Most of the time it's that you used one pin for both the display, button or LED.  
Be sure not to have used the same pin for multiple things, not on the breadboard and not in the code!  

Still no image on the diplay? Type in `set display true;;save settings` and press enter. Now press the reset button on the board to restart it. If the dislpay doesn't show anything, something is off. Check your connections and your code!  

To see if all buttons are working correctly use the `screen mode buttontest` command. To get back use `screen mode menu`.  

If you have problems with the display, try using other software that uses the display. That way you will know if it's a software or a hardware problem.  
Here's the display library used for the deauther: https://github.com/squix78/esp8266-oled-ssd1306  
You can find examples there, try to get those running.  

To test the LED(s), you can use the `led <r> <g> <b>` command. For example `led 255 0 0` should turn on only the red LED.   

---

{{< footerbuttons >}}