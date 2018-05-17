---
title: Virtual Box basic commands
date: 2018-05-17 09:21:07
categories: [devops]
tags: [bash, virtual box]
author: sedlav
---

## Start a VM
```
$ vboxmanage startvm "VM Name"
```

## Power off the VM
```
$ vboxmanage controlvm "VM Name" poweroff
```

## Show VM info
```
$ vboxmanage showvminfo "VM Name"
```

## Register/Add a VM
```
$ vboxmanage registervm "full path to .vbox file"
```

## Unregister/Add a VM
```
$ vboxmanage unregistervm "VM Name"
```

## Delete a VM
```
$ vboxmanage unregistervm --delete "VM Name"
```
