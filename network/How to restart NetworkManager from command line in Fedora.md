---
title: "How to restart NetworkManager from command line in Fedora?"
date: 2017-11-21 09:52:34
categories: [network]
tags: [networkmanager]
author: sedlav
---

Q. I've using Fedora 24 and sometimes my network connection go idle, losing my internet connection or name server resolution then I need to restart my OS. Can I restart my network connection without restarting the OS?

A. Yes, you can type.

```bash
$ sudo systemctl restart NetworkManager
```
