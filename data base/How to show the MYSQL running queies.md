---
title: "How to show the MYSQL running queies"
date: 2020-01-09 18:49:13
categories: [data base]
tags: [mysql, mariadb, percona]
author: sedlav
---

`SHOW PROCESSLIST` shows you which threads are running. You can also get this information from the INFORMATION_SCHEMA PROCESSLIST table or the mysqladmin processlist command. If you have the PROCESS privilege, you can see all threads. Otherwise, you can see only your own threads (that is, threads associated with the MySQL account that you are using)

## Syntax

```mysql
SHOW [FULL] PROCESSLIST
```
