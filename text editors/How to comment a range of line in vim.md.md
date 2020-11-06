---
title: "How to comment a range of line in vim?"
date: 2020-11-06 05:47:31
categories: [text editors]
tags: [vim]
author: sedlav
---

In modal mode press:

## For uppercase

```
:start_line, end_lines/\(.*\)/#\1/
```