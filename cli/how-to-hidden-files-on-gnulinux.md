---
title: "How to find hidden files on GNU/Linux?"
date: 2018-10-23 17:08:13
categories: [cli]
tags: [find]
authors: sedlav
---

You must use the **find** command, for example find all hidden file in our $HOME

```
$ find $HOME -maxdepth 1 -name ".*" -type f  -ls
```
