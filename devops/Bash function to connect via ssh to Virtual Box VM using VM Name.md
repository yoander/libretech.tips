---
title: Bash function to connect via ssh to Virtual Box VM using VM Name
date: 2017-12-08 12:12:07
categories: [devops]
tags: [bash, virtual box, ssh]
author: sedlav
---

This a bash function that allows to connect to a Virtual Box VM using VM Name, for example: vbossh centos

```bash
#
#
# Connect to VM by VM Name via shh if user is not specified
# then try to connect using root user
# Examples: vboxssh root@CentOS7, vboxssh CentOS7
#
function vboxssh {
    USER=
    if [[ "$1" == *@* ]]; then
        # Get the user for ssh connection
        USER=$(echo $1|cut -d@ -f1) || $(echo root)
    fi
    if [[ "$USER" == "" ]]; then
        USER=root
    fi 
    # Get the VM Name
    VM=$(echo $1|cut -d@ -f2)
    # Verify the VM exists
    if [[ $(vboxmanage list vms|grep -c "\"$VM\"") == 0 ]]; then
        echo $VM virtual machine does no exist
        return 1
    fi
    # Check if the VM if running else try to start in headless mode
    if [[ $(vboxmanage list runningvms|grep -c "\"$VM\"") == 0 ]]; then 
        echo Starting virtual machine: "$VM" in headless mode
        vboxmanage startvm "$VM" -type headless
    fi
    # Get the MAC address, credit to: https://serverfault.com/a/540115/440475
    MAC=$(vboxmanage showvminfo "$VM" --details 2>&1 | grep 'NIC 1:' | sed -re 's/.*MAC: (.+), Attachment.*/\1/' -e 's/(\w{2})/\1:/g' -e 's/:$//')
    # Get the IP Address for the VM
    IP=
    retry=1
    # Until IP is got or time >= 5m
    while [[ $IP == "" ]] && [[ $retry -lt 61 ]]
    do
        echo Trying to get VM IP address, retry: $retry
        IP=$(ip neighbor |grep -i "$MAC"|awk '{print $1}')
        # IF we can't get IP sleep for 5s and try again
        if [[ $IP == "" ]]; then
            (( ++$retry ))
            sleep 5s
        else
            retry=6;
        fi
    done
    if [[ $IP == "" ]]; then
        echo We can not determine the VM IP
        return 2
    fi
    retry=1
    # Connect via ssh
    # VM are trusted env when connecting from the host then we can add these
    # options to the ssh client
    while ! ssh $USER@$IP -o "StrictHostKeyChecking no" -o "CheckHostIP no" && [[ $retry -lt 61 ]]; do
        echo Waiting VM start ssh service
        (( ++$retry ))
        sleep 5s;
    done
}
```

⋔ me on [Github](https://gist.github.com/yoander/19971f603ecd850182e4f2a7875bebf9) 
