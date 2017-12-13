---
title: "MySQL cache configuration examples"
date: 2017-11-28 11:25:43
categories: [data base]
tags: [mysql, mariadb, percona]
author: sedlav
---

This is a MySQL cache configuration example for a server with CPU: Core 2 Quad Q6600 2.4 GHZ, RAM: 4GB for a site with +5000 unique visits per day (Use it at your own risk).

```
query_cache_type=1
query_cache_size=512M
thread_cache=64
thread_cache_size=256
table_cache=1024
key_buffer_size=512M
tmp_table_size=256M
max_heap_table_size=256M
join_buffer_size=5M
```
