---
title: "How to test NGINX configuration file"
date: 2017-11-20 11:33:02
categories: [web server]
tags: [nginx]
author: sedlav
---

## Test configuration and exit

```nginx
$ sudo nginx -t
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
```

## Show version and configure options then exit

```nginx
$ sudo nginx -V
nginx version: nginx/1.12.2
built by gcc 4.4.7 20120313 (Red Hat 4.4.7-18) (GCC) 
built with OpenSSL 1.0.1e-fips 11 Feb 2013
TLS SNI support enabled
configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx -
...
```

## Further reading

* nginx -h
