---
title: How to get the full path of a command on GNU/Linux?
date: 2017-12-10 11:45:19
categories: [cli]
tags: [which]
slug: how-to-get-the-full-path-of-a-command-on-gnulinux
authors: sedlav
---

You must use the **which** command:

```
$ which ls
alias ls='ls --quoting-style=literal --color'
/usr/bin/ls
```
