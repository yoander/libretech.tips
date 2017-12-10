---
title: How to watch for specific pattern in a log file.
date: 2017-12-10 11:44:09
categories: [cli]
tags: [tail, grep]
authors: sedlav
---

You must combine tail and grep in this way:

```
# tail -f log_file | grep pattern
```

For example watch for a specific IP in the Apache log.

```
# tail -f /var/log/httpd/access_log | grep IP-address
```
