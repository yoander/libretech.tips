---
title: "How to execute PHP simple code from the command line?"
date: 2018-01-12 18:21:28
categories: [programming]
tags: [php]
authors: sedlav
---

Use the **-r** option.

```
$ php -r 'var_dump(count(["a"=>[1,2,3],"b"=>[4,5,6]]));'
Command line code:1:
int(2)
```

## Further reading

```
php -h
```