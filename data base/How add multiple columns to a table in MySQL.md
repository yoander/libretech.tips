---
title: "How add multiple columns to a table in MySQL"
date: 2020-10-29 10:49:39
categories: [data base]
tags: [mysql, mariadb, percona]
author: sedlav
---

`ALTER TABLE` changes the structure of a table. For example, you can add or delete columns, create or destroy indexes, change the type of existing columns, or rename columns or the table itself. You can also change characteristics such as the storage engine used for the table or the table comment.

In this case we're going to add multiple columns at the same time

## Syntax

```mysql
ALTER TABLE my_table_name ADD COLUMN (column1, column2, ...)
```

## Example

```mysql
ALTER TABLE libretech.post  ADD COLUMN (`label` varchar(120) DEFAULT NULL, `desc` text, `options` text)
```

In the previous example 3 columns will be added to the post table after the last column, post table belongs to libretech DB.


<?php
if ($a->sssss) {

}
