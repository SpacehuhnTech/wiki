---
title: "Deauth-Attack not working"
date: 2020-09-25T13:16:10+02:00
weight: 10 # The smaller the higher position in the navigation and vice versa
tags: []
---

Here are some possible reasons:<p />
- maybe the device connects too fast, try increasing the pkts/s in the settings<p />
- maybe the network is 5ghz, the ESP can only do 2.4ghz<p />
- maybe 802.11w standart alias protected management frames are activated on your network,<p />
this means you can't fake them and your network is safe against deauth attacks

---

{{< footerbuttons >}}