---
title: "When a MYSQL table was created.?"
date: 2020-01-16 10:14:22
categories: [data base]
tags: [mysql, mariadb, percona]
author: sedlav
---

MYSQL stores tables information on `TABLES` table under `information_schema` data base, so you can use a sentence like this to get when a tables was created

```mysql
SELECT `CREATE_TIME` FROM `TABLES` WHERE `TABLE_NAME` = 'my-table-name'
```

If you have the same table name on different data base then you can use this query:

```mysql
SELECT `CREATE_TIME` FROM `TABLES` WHERE `TABLE_SCHEMA` = 'my-database-name' AND `TABLE_NAME` = 'my-table-name'
```