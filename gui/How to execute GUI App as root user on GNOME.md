---
title: How to execute GUI App as root user on GNOME
date: 2020-09-24 16:34:51
categories: [gui]
tags: [pkexec, flatpak]
author: sedlav
---

## Run gedit

```
$ pkexec gedit
```

## Run a flatpak app (Wireshark)

```
$ pkexec env DISPLAY=$DISPLAY XAUTHORITY=$XAUTHORITY flatpak run --system org.wireshark.Wireshark
```
