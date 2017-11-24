---
title: Find files and perform an action on them
date: 2017-11-23 23:35:20
categories: [cli]
tags: [find, while]
slug: find-files-and-perform-an-action-on-them
author: sedlav
---

```bash
$ find DIR -name filename -type f -print0  | while read -d $'\0' file; do echo $file; done
```
