---
title: "How to redirect from http to https in Apache?"
date: 2017-07-27 08:30:57
categories: [web server]
tags: [apache]
author: sedlav
---

You can redict from http to https in apache adding the following direcitive inside your virtual host.


```apache
RedirectMatch "^(.*)$" "https://newdomain.com$1" 
```

## Further reading

* [RedirectMatch](http://httpd.apache.org/docs/2.4/mod/mod_alias.html#redirectmatch)
