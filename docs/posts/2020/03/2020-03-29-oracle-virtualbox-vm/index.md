---
title: "Oracle VirtualBox™ &amp; VMware Photon OS™"
date: 2020-03-29
categories: 
  - "vizz"
tags: 
  - "distro"
  - "oracle"
  - "ova"
  - "photon"
  - "photon-os"
  - "virtualbox"
  - "vm"
  - "vmware"
---

Oracle VirtualBox™ & VMware Photon OS™

None of the VMware Photon OS™ OVA work on virtual box

- http://dl.bintray.com/vmware/photon/3.0/Rev2/ova/photon-hw11-3.0-9355405.ova
- http://dl.bintray.com/vmware/photon/3.0/Rev2/ova/photon-hw13\_uefi-3.0-9355405.ova

instead use the VMware Photon OS™ for @foldingathome

- https://flings.vmware.com/vmware-appliance-for-folding-home

Boot it and change root password by typing E etc as per ([how to change gnu/linux root password](https://vizz8info.wordpress.com/2020/03/28/vmware-photon-os/))

You could also try the ISO

- http://dl.bintray.com/vmware/photon/3.0/Rev2/iso/Update1/photon-minimal-3.0-a0f216d.iso

Once you get PH working it has avery clean install

```
$ cat /etc/passwd
root:x:0:0:root:/root:/bin/bash
bin:x:1:1:bin:/dev/null:/bin/false
daemon:x:6:6:Daemon User:/dev/null:/bin/false
messagebus:x:18:18:D-Bus Message Daemon User:/var/run/dbus:/bin/false
systemd-bus-proxy:x:72:72:systemd Bus Proxy:/:/bin/false
systemd-journal-gateway:x:73:73:systemd Journal Gateway:/:/bin/false
systemd-journal-remote:x:74:74:systemd Journal Remote:/:/bin/false
systemd-journal-upload:x:75:75:systemd Journal Upload:/:/bin/false
systemd-network:x:76:76:systemd Network Management:/:/bin/false
systemd-resolve:x:77:77:systemd Resolver:/:/bin/false
systemd-timesync:x:78:78:systemd Time Synchronization:/:/bin/false
nobody:x:65534:65533:Unprivileged User:/dev/null:/bin/false
sshd:x:50:50:sshd PrivSep:/var/lib/sshd:/bin/false
fahclient:x:999:100:Folding@home Client:/var/lib/fahclient:/sbin/nologin
cdarra:x:1000:100::/home/cdarra:/bin/bash

cdarra@vghetto-photonos [ / ]$ ls -l
total 44
lrwxrwxrwx 1 root root 7 May 10 2019 bin -> usr/bin
drwxr-xr-x 4 root root 4096 Mar 22 23:04 boot
drwxr-xr-x 15 root root 3480 Mar 29 09:47 dev
drwxr-xr-x 42 root root 4096 Mar 29 09:55 etc
drwxr-xr-x 2 root root 4096 May 10 2019 home
lrwxrwxrwx 1 root root 7 May 10 2019 lib -> usr/lib
lrwxrwxrwx 1 root root 7 May 10 2019 lib64 -> usr/lib
drwx------ 2 root root 16384 Mar 22 22:38 lost+found
lrwxrwxrwx 1 root root 9 May 10 2019 media -> run/media
drwxr-xr-x 4 root root 4096 Mar 22 22:38 mnt
dr-xr-xr-x 94 root root 0 Mar 29 09:47 proc
drwxr-x--- 5 root root 4096 Mar 29 09:55 root
drwxr-xr-x 17 root root 480 Mar 29 09:49 run
lrwxrwxrwx 1 root root 8 May 10 2019 sbin -> usr/sbin
lrwxrwxrwx 1 root root 7 May 10 2019 srv -> var/srv
dr-xr-xr-x 13 root root 0 Mar 29 09:47 sys
drwxrwxrwt 10 root root 200 Mar 29 09:56 tmp
drwxr-xr-x 10 root root 4096 Mar 22 22:38 usr
drwxr-xr-x 12 root root 4096 Mar 22 23:02 var
```

Startup screenshot

![VirtualBox_fah_29_03_2020_10_38_35.png](https://vizz8info.wordpress.com/wp-content/uploads/2020/03/virtualbox_fah_29_03_2020_10_38_35.png)
