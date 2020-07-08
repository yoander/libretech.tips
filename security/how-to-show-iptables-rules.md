---
title: "How to show iptables rules"
date: 2020-07-08 10:33:53
categories: [security]
tags: [firewall, rhel, iptables]
authors: sedlav
---

Type the following command as root user

```
$ sudo iptables -L
```

**nat** table rules is not show by dafault so you need to execute

```
$ sudo iptables -t nat -L
```

## Further reading

- man iptables
