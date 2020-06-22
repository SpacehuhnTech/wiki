---
title: "Web"
date: 2020-06-18T14:02:46+02:00
weight: 1 # The smaller the higher position in the navigation and vice versa
tags: []
---
## Getting Started

1) Scan for WiFi networks.
2) Connect to `pwned` with the password `deauther`.  
3) Open 192.168.4.1 (or deauth.me)

If you don't see a `pwned` network, flash the ESP8266 again. See [installation](https://github.com/spacehuhn/esp8266_deauther/wiki/Installation) for more.  
You can also look at the [Serial monitor](https://github.com/spacehuhn/esp8266_deauther/wiki/Serial) for further debugging.  

## A Few Notes
Ok so a few things people like to complain about that are perfectly normal.

**1.** The web interface is unstable and gives errors.  
Yes it does, the web server is build with an outdated library that is known to cause some trouble. 
We can't do much about it but we're trying to get the best performance out of it. Errors do happen, but that shouldn't bother you too much as long as everything works like it should.  

**2.** I lose connection when scanning or attacking.  
Yep. Both for attacking and searching for WiFi stations, the device has to do channel hopping and can not host a network itself.  

Keep in mind that you can always use the [display interface](https://github.com/spacehuhn/esp8266_deauther/wiki/Display) or the [serial interface](https://github.com/spacehuhn/esp8266_deauther/wiki/Serial) for more capabilities and better performance :).  

## Home Page

Once you opened the web interface, you should see this warning page.  
Please read the disclaimer carefully before going on by clicking the button below.  

![PICTURE home/warning page](/media/deauther/home_page.jpg?height=400px)

## Scan Page

Here you can start scanning for access points (WiFi networks) and Stations (Client devices).  
Usually you want to start by scanning for access points first and see how much networks are around you.  
Please note that the scan takes a few seconds (usually 2 - 5 seconds). You should see a LED going on when starting the scan. When it goes off, the scan is done and you can hit *Reload* to load the scan results.  

![PICTURE scan page 1](/media/deauther/scan_page_1.jpg?height=400px)

Now you can go through the list and select the networks you want to attack.  

![PICTURE scan page 2](/media/deauther/scan_page_2.jpg?height=400px)

## SSID Page

Here you can add, edit and remove SSIDs. These SSIDs are used for the beacon and probe attack.  

![PICTURE SSID page 1](/media/deauther/ssid_page_1.jpg?height=435px)  

![PICTURE SSID page 2](/media/deauther/ssid_page_2.jpg?height=400px)  

## Attack page

Here is where you actually start attacking WiFi devices. Now keep in mind that when starting an attack, you can loose the connection to the web interface! But if you only select one target, you should be able to reconnect to it without problems.   
Like on the scan page, it is important that you manually click *Reload*. This is made on purpose to save ressources and help the stability of the web server.  

![PICTURE attack page](/media/deauther/attack_page.jpg?height=400px)

## Settings page

Edit the settings you like to change, click *Save* and *Reload* to confirm your changes were applied.  

![PICTURE settings page](/media/deauther/settings_page.jpg?height=400px)

---

{{< footerbuttons >}}