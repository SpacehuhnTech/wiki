---
title: "Troubleshooting"
date: 2020-10-09T13:21:06+02:00
weight: 10 # The smaller the higher position in the navigation and vice versa
tags: []
---

these are some problems you might encounter and what you can do to fix them

{{% collapsible "Deauth-Attack not working" %}}
Here are some possible reasons:<p />
- maybe the device connects too fast, try increasing the pkts/s in the settings<p />
- maybe the network is 5ghz, the ESP can only do 2.4ghz<p />
- maybe 802.11w standart alias protected management frames are activated on your network,<p />
this means you can't fake them and your network is safe against deauth attacks
{{% /collapsible %}}

---

{{< footerbuttons >}}