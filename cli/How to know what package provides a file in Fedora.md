---
title: How to know what package provides a file in Fedora?
date: 2017-12-10 12:03:35
categories: [cli]
tags: [whereis, dnf]
authors: sedlav
---

First locate the executable with

```
$ whereis executable
```

Example

```
$ whereis nc
nc: /usr/bin/nc /usr/share/man/man1/nc.1.gz
```

Second

```
$ sudo dnf provides nc
Last metadata expiration check: 1:12:35 ago on Sun Dec 10 10:40:50 2017.
nmap-ncat-2:7.40-1.fc24.x86_64 : Nmap's Netcat replacement
Repo        : @System

nmap-ncat-2:7.12-1.fc24.x86_64 : Nmap's Netcat replacement
Repo        : fedora

nmap-ncat-2:7.40-1.fc24.x86_64 : Nmap's Netcat replacement
Repo        : updates

```

### Further reading:

* man id
