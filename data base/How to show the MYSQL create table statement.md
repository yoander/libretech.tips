---
title: "How to show the MYSQL create table statement"
date: 2020-06-08 16:05:12
categories: [data base]
tags: [mysql, mariadb, percona]
author: sedlav
---

`SHOW CREATE TABLE tbl_name` Shows the CREATE TABLE statement that creates the named table. To use this statement, you must have some privilege for the table. This statement also works with views.

## Syntax

```mysql
SHOW CREATE TABLE tbl_name
```

## Example

```mysql
mysql> SHOW CREATE TABLE t\G
*************************** 1. row ***************************
       Table: t
Create Table: CREATE TABLE `t` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `s` char(60) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4
```
