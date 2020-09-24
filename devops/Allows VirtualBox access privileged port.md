---
title: Allows VirtualBox access privileged port
date: 2020-09-05 16:30:23
categories: [devops]
tags: [virtual box]
author: sedlav
---

Ir order to allow VirtualBox redirect/access priveleges port you need to set this enviroment variable

```
export VBOX_HARD_CAP_NET_BIND_SERVICE=1
```

### Sources

- [Using setcap to listen on privileged ports?](https://forums.virtualbox.org/viewtopic.php?t=45481)
- [VirtualBox Host Driver Source Code](https://www.virtualbox.org/browser/vbox/trunk/src/VBox/HostDrivers/Support/SUPR3HardenedMain.cpp?rev=77912#L1958)