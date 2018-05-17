---
title: "How to print the date in UTC on GNU/Linux?"
date: 2017-12-22 18:14:02
categories: [cli]
tags: [date]
authors: sedlav
---

You must use the date command in this way

```
$  date -u +'%Y-%M-%d %H:%m:%S UTC'
2017-10-22 23:12:07 UTC
```

## Further reading

- man date
