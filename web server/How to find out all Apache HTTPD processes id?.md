---
title: "How to find out all Apache HTTPD processes id?"
date: 2017-12-20 09:57:05
categories: [web server]
tags: [apache]
author: sedlav
---

You can find out all Apache HTTPD processes id typing:


```bash
$ pidof httpd
24599 24576 24532 14467 10240 1248 1242 1215 1214 1213 1106
```

Or

```bash
pgrep -x httpd
1106
1213
1214
1215
1242
1248
10240
14467
24532
24576
24599
```

In Fedora >= 24 you can type

```bash
$ sudo apachectl status
● httpd.service - The Apache HTTP Server
   Loaded: loaded (/usr/lib/systemd/system/httpd.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-12-18 08:51:00 -05; 2 days ago
     Docs: man:httpd.service(8)
 Main PID: 1106 (httpd)
   Status: "Total requests: 393; Idle/Busy workers 100/0;Requests/sec: 0.00222; Bytes served/sec: 200 B/sec"
    Tasks: 77 (limit: 512)
   CGroup: /system.slice/httpd.service
           ├─ 1106 /usr/sbin/httpd -DFOREGROUND
           ├─ 1213 /usr/sbin/httpd -DFOREGROUND
           ├─ 1214 /usr/sbin/httpd -DFOREGROUND
           ├─ 1215 /usr/sbin/httpd -DFOREGROUND
           ├─ 1242 /usr/sbin/httpd -DFOREGROUND
           ├─ 1248 /usr/sbin/httpd -DFOREGROUND
           ├─10240 /usr/sbin/httpd -DFOREGROUND
           ├─14467 /usr/sbin/httpd -DFOREGROUND
           ├─24532 /usr/sbin/httpd -DFOREGROUND
           ├─24576 /usr/sbin/httpd -DFOREGROUND
           └─24599 /usr/sbin/httpd -DFOREGROUND
```
