---
title: "How to disable SELinux in CentOS / RHEL / Fedora"
date: 2017-12-17 00:37:04
categories: [security]
tags: [centos, fedora, rhel, selinux]
slug: how-to-disable-selinux-in-centos-rhel-fedora
authors: sedlav
---

To disable the SELinux, you must edit the /etc/sysconfig/selinux file and set SELINUX=disabled

```
$ cat /etc/sysconfig/selinux
# This file controls the state of SELinux on the system.
# SELINUX= can take one of these three values:
#     enforcing - SELinux security policy is enforced.
#     permissive - SELinux prints warnings instead of enforcing.
#     disabled - No SELinux policy is loaded.
SELINUX=disabled
# SELINUXTYPE= can take one of these three values:
#     targeted - Targeted processes are protected,
#     minimum - Modification of targeted policy. Only selected processes are protected.
#     mls - Multi Level Security protection.
SELINUXTYPE=targeted
```
