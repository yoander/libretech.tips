---
title: "What database and table a column belongs to in MySQL"
date: 2020-06-08 18:19:26
categories: [data base]
tags: [mysql, mariadb, percona]
author: sedlav
---

If you want to locate a column in MySQL you can use the following query

```mysql
SELECT `TABLE_SCHEMA`, `TABLE_NAME`, `COLUMN_NAME` FROM information_schema.`COLUMNS` WHERE `COLUMN_NAME` = 'my-colum-name'
```

Also you can use the `LIKE` operator

```mysql
SELECT `TABLE_SCHEMA`, `TABLE_NAME`, `COLUMN_NAME` FROM information_schema.`COLUMNS` WHERE `COLUMN_NAME` LIKE '%my-colum-pattern%'
```
