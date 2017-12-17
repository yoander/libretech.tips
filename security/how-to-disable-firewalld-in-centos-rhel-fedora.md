---
title: "How to disable Firewalld in CentOS / RHEL / Fedora"
date: 2017-12-17 00:36:50
categories: [security]
tags: [centos, fedora, firewalld, rhel]
slug: how-to-disable-firewalld-in-centos-rhel-fedora
authors: sedlav
---

I do not recommend to disable the firewall on server but if you are doing some testing then you can disable using the following command:

Type the following command in your console

```
$ sudo systemctl disable firewalld.service
```

You can view the service status with:

```
$ systemctl status firewalld.service
● firewalld.service - firewalld - dynamic firewall daemon
Loaded: loaded (/usr/lib/systemd/system/firewalld.service; disabled; vendor p
Active: inactive (dead)
Docs: man:firewalld(1)
```
