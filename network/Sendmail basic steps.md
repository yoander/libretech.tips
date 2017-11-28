---
title: "Sendmail basic steps"
date: 2017-11-28 00:23:03
categories: [network]
tags: [sendmail, smtp, email]
author: sedlav
---

**Sendmail** is a general purpose internetwork email routing facility that supports many kinds of mail-transfer and delivery methods, including the Simple Mail Transfer Protocol (SMTP) used for email transport over the Internet.

## Install on CentOS/RHEL

```bash
# yum install sendmail sendmail-cf
```

## File alias definition

```bash
#  cat /etc/aliases 
```

## Rebuild database of aliases

```bash
# newaliases
```

## Mailer table

```bash
# makemap hash /etc/mail/mailertable < /etc/mail/mailertable
```

## Access table

```bash
# makemap hash /etc/mail/access < /etc/mail/access 
```

## Virtual User/Domain table

```bash
# makemap hash /etc/mail/virtuser < /etc/mail/virtuser
```