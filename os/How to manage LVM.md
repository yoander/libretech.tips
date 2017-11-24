---
title: How to manage LVM
date: 2017-11-24 11:50:06
categories: [os]
tags: [lvm]
author: sedlav
---

LVM management:

## Groups

### Create
```bash
# vgcreate <physical volumen|device>
```

### List
```bash
# vgs
```

### Info
```bash
# vgdisplay
```

## PV (Physical volumes)

### Create
```bash
 # pvcreate <device|partition>
```

### List
```bash
# pvs
```

### Info
```bash
 # pvdisplay
```

## LV (Logical volume)

### Create
```bash
# lvcreate -L 30G -n logical-volumen-name group name
```

### List
```bash
# lvs
```

### Info
```bash
# lvdisplay
```

### Format
```bash
# mkfs.ext3 -m 0 /dev/group-name/logical-volumen-name   [-L label]
```

### Mount

Add to /etc/fstab
```
/dev/group-name/logical-volumen-name      /mnt/some-dir             ext3    defaults,acl    1 2 (ACL is optional)
```

Or

```
 LABEL=label                             /mnt/some-dir              ext3    defaults,acl    1 2 (ACL is optional)
 ```