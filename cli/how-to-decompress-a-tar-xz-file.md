---
title: "How to decompress a tar.xz file?"
date: 2017-12-10 11:44:43
categories: [cli]
tags: [tar]
slug: how-to-decompress-a-tar-xz-file
authors: sedlav
---

You must use the tar tool with J option

```
$ tar xJvf php-7.0.10.tar.xz</code></pre>
```

Where:

x = extract
f = file
v = verbose
J = Filter the archive through xz
