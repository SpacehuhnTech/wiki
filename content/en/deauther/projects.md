---
title: "Projects"
date: 2020-06-11T17:00:17+02:00
weight: 6 # The smaller the higher position in the navigation and vice versa
tags: []
---

**A collection of cool projects people made with the ESP8266 Deauther.**


I hope this gives some inspiration and motivation to make/hack something together yourself :)  
If you have a cool project that isn't listed here, let me know to add it by tweeting me [@spacehuhn](http://github.com/spacehuhn/)!

- [Deauthing Sandals](#deauthing-sandals)
- [Drone Hacking a FAKE Makerspace](#drone-hacking-a-fake-makerspace)
- [Deauther Magnet Box for Fridge](#deauther-magnet-box-for-fridge)
- [Deauth Detector with 10W RGB](#deauth-detector-with-10w-rgb)
- [Pwned the pwner](#pwned-the-pwner)

### Deauthing Sandals
Becky Button [@einsteinunicorn](https://twitter.com/einsteinunicorn) in collaboration with Naomi Wu [@RealSexyCyborg](https://twitter.com/RealSexyCyborg) designed and 3D printed a sandal. They put the ESP8266 Adafruit Feather HUZZAH in it, together with a LiPo battery to power it. 
A truly fun project that shows that you can put an ESP8266 everywhere!
- 📺 [YouTube](https://www.youtube.com/watch?v=XHkkO97mxTk)
- [hackster.io](https://www.hackster.io/58569/wi-fi-deauthing-sandals-540e3b)
- [Adafruit](https://blog.adafruit.com/2017/09/27/wi-fi-deauthing-sandals-wearablewednesday/)
- [Reddit](https://www.reddit.com/r/hacking/comments/7227un/high_school_girl_builds_esp8266_into_deauth/)

### Drone Hacking a FAKE Makerspace
Naomi Wu [@RealSexyCyborg](https://twitter.com/RealSexyCyborg) had fun annoying a fake Makerspace in Shenzhen using a drone that drops an ESP8266 to send a bunch of SSIDs.
She used the [beacon-spam](https://github.com/spacehuhn/esp8266_beaconSpam) code for this but you can do the same thing with the deauther and a autostart script.
- 📺 [YouTube](https://www.youtube.com/watch?v=Cdk4Zw2oYdc)

### Deauther Magnet Box for Fridge
[Tobozo](https://twitter.com/TobozoTagada) designed, printed and filled this nice box with an ESP8266 board, a 18650 Li-ion, a battery charger, a big 2.4 inch OLED, an on/off switch, a thumbstick and a few magnets to stick the whole box on the fridge!
- 📺 [Youtube](https://www.youtube.com/watch?v=bNIh7MjtLx8)
- [Thingiverse](https://www.thingiverse.com/thing:2781867)

### Deauth Detector with 10W RGB
Just a short video to show you that with the version 2.0, you can connect all kinds of LEDs!
I have a simple standalone [DeauthDetector](https://github.com/spacehuhn/DeauthDetector) script but here I used the deauther 2.0 as it has a build-in support for different LEDs and can also detect deauthentication frames when scanning.
- 📺 [Youtube](https://www.youtube.com/watch?v=sPGe1WIt5kA)

### Pwned the pwner
Dave [@davedarko](https://twitter.com/davedarko) shows you in this quick video that changing the default password and SSID is a good idea! He made a script that searches for deauthers and try to log into them with the default credentials. When it's successful it will change the SSID and password and send a restart request.
But please note that this script was made for the 1.6 version and would need a few adjustments to work against the version 2.0.
- 📺 [YouTube](https://www.youtube.com/watch?v=D8zmXoDFpjU)
- :octocat: [Source Code](https://gist.github.com/davedarko/87183b00e77ffb8fc59f89bf3b23d561)

---

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for deauther/projects.md&body=I'd like to suggest changes for `deauther/projects.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki/deauther/projects)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/projects.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/projects.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}