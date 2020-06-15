---
title: "Development"
date: 2020-06-07T22:38:56+02:00
weight: 16 # The smaller the higher position in the navigation and vice versa
tags: []
---

### Edit Web Files

If you would like to modify the web interface, you can!  
The `web/` folder contains all `.html`, `.css`, `.js` files.  
You can edit and test them locally as long as you're connected to the WiFi Duck
network thanks to the websocket connection handled by JavaScript in the background.  

To get the new files onto the ESP8266, run `python3 webconverter.py` in the
repository folder.  
It gzips all files inside `web/`, converts them into a hex array
and saves it in `esp_duck/webfiles.h`.  
Now you just need to [flash](#flash-software) the ESP8266 again.  

---

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for /wifiduck/content/development.md&body=I'd like to suggest changes for `/wifiduck/content/development.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki//wifiduck/content/development)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/main/content/en//wifiduck/content/development.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/main/content/en//wifiduck/content/development.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}