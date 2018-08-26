---
title: "How to know the ip address of my server?"
date: 2017-11-21 22:47:27
categories: [network]
tags: [ip]
author: sedlav
---

To know the ip address from the command line you can type:

* For ipv4 

```bash
$ ip -f inet a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
3: wlp2s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
    inet 192.168.100.4/24 brd 192.168.100.255 scope global dynamic wlp2s0
```

* For ipv6

```bash
$ ip -f inet6 a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 state UNKNOWN qlen 1000
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
3: wlp2s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 state UP qlen 1000
    inet6 fe80::52b7:c3ff:fe45:f086/64 scope link 
```
