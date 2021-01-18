---
title: "How to kill a MySQL query?"
date: 2021-01-18 09:39:07
categories: [data base]
tags: [mysql, mariadb, percona]
author: sedlav
---

First you need to identify the query with [SHOW PROCESSLIST](/data-base/how-to-show-the-mysql-running-queries/) and execute a KILL with the query id.

```mysql
KILL query-id
```