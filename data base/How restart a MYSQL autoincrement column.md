---
title: "How restart a MYSQL autoincrement column?"
date: 2020-01-11 18:13:34
categories: [data base]
tags: [mysql, mariadb, percona]
author: sedlav
---

Use `ALTER TABLE` to restart a autoincrement column

## Syntax

```mysql
ALTER TABLE tb_name AUTO_INCREMENT = new_index
```
