---
title: "How to create a  file on the fly on GNU/Linux?"
date: 2017-12-10 20:02:22
categories: [cli]
tags: [touch]
slug: how-to-create-file-on-the-fly-on-gnulinux
authors: sedlav
---

You must use the **touch** command or **>** operator, the touch command will create an empty file while **>** also can put content on the file

###  Using touch command:

```
$ touch emptyfile.txt
```

### Using output redirector operator

```
$ echo -e "This an empty file\nwith a new line" > emptyfile.txt
```
