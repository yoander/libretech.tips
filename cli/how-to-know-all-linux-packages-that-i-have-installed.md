---
title: How to know all Linux packages that I have installed?
date: 2017-12-10 11:45:59
categories: [cli]
tags: [dpkg-query]
slug: how-to-know-all-linux-packages-that-i-have-installed
authors: sedlav
---

If you are using Debian base distro you can type:

```
$ sudo dpkg-query -l '*linux*'
...
ii  linux-image-4.4.0-34-generic           4.4.0-34.53~14.04.1
ii  linux-image-extra-4.4.0-34-generic     4.4.0-34.53~14.04.1
ii  linux-image-generic-lts-xenial         4.4.0.34.24
...
```
