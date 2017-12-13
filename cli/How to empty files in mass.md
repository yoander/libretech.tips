---
title: How to empty files in mass?
date: 2017-11-22 22:27:02
categories: [cli]
tags: [find, xargs, bash]
authors: sedlav
---

If you want to empty several files in one operation you can type a sentence like this

```bash
$  find -type f -name '*.xml' -print0|xargs -0 -I {} bash -c "> {}"
```
