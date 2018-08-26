---
Title: How to remove a file with a dash at the beginning of the name?
Date: 2017-12-10 11:49:25
Categories: [cli]
tags: [rm]
Slug: how-to-remove-a-file-with-a-dash-at-the-beginning-of-the-name
Authors: sedlav
---

You must use a double dash before the file name.

```
$ rm -- -Rfv
```

The above example removes a file named: -Rfv.
