---
title: "how to login to an oracle cloud instance without user password or ssh key"
date: 2024-10-16
categories: 
  - "vizz"
tags: 
  - "devops"
  - "login"
  - "ssh"
  - "sysadmin"
---

how to login to an oracle cloud instance without password or ssh key

bring up two browser tabs/windows

[https://cloud.oracle.com/compute/instances?region=uk-london-1](https://cloud.oracle.com/compute/instances?region=uk-london-1)

choose the same instance in both

open console in second tab

reboot instance in first tab

as soon as terminal console goes blank press downarrow until grub menu appears

choose a boot option

press "e"

go down to the line beginning linux

go to the end of the line and append "init=/bin/bash"

press CTRL-X

after a while you should get a bash prompt

```
# mount -o remount,rw /
# cd ~opc/.ssh

# passwd opc
NEWPWD

# vi authorized_keys 
and add new public key

# /usr/sbin/reboot -f
```

[https://docs.oracle.com/en-us/iaas/Content/Compute/References/serialconsole.htm](https://docs.oracle.com/en-us/iaas/Content/Compute/References/serialconsole.htm)
