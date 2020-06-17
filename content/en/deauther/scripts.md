---
title: "Writing Scripts"
date: 2020-06-11T17:01:40+02:00
weight: 8 # The smaller the higher position in the navigation and vice versa
tags: []
---

[![Video on scripting with deauther 2.0](https://img.youtube.com/vi/v8xkyR3JXrw/0.jpg)](https://www.youtube.com/watch?v=v8xkyR3JXrw)

### Introduction

One cool thing about the new deauther version is the ability to write scripts. This is meant as a small add-on, and not as a main feature. You can't really program with it or do complicated stuff, and all you can do is save regular commands to a file. To show you this, I will demonstrate how to deauth a specific mac address using a script. The only caveat here is that you need to know the channel. First, we're going to create a file on the ESP using: <br>
`write deauthmac.txt send deauth FF:FF:FF:FF:FF:FF FF:FF:FF:FF:FF:FF 0 1`
The first broadcast MAC is the access point MAC, and the second is the MAC of the station. The first 0 is the reason (0 is unspecified) and the second 0 is the channel. As I said before, you have to know the channel your target is on, but if you want to get around this, you could just make the same command 14 times, incrementing the channel from 1-14. 

### Running on boot
To run your script on boot, write it to autostart.txt instead of another file. One caveat to this system is that there is currently **NO RUN COMMAND WITHIN SCRIPTS**, Meaning that you can't run a script from within a script. 

---

{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for deauther/scripts.md&body=I'd like to suggest changes for `deauther/scripts.md`%0A%0A:link: [Wiki](https://spacehuhn.wiki/deauther/scripts)%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/scripts.md)%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/master/content/en/deauther/scripts.md" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}