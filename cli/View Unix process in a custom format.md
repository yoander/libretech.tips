---
title: "View Unix process in a custom format"
date: 2017-09-25 16:32:19
categories: [cli]
tags: [ps]
author: sedlav
---

You can view process in a custom format typing:

```
$ ps -U username -u username  -o pid,cmd

$ ps -U mysql -u mysql -o pid,cmd
  PID CMD
 1304 /usr/sbin/mysqld --daemonize --pid-file=/var/run/mysqld/mysqld.pid
```

## Further reading

* man ps
