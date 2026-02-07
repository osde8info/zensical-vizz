---
title: "gNewSense &amp; Xubuntu VMware guest clock loses time"
date: 2007-09-13
categories: 
  - "vizz"
---

gNewSense & Xubuntu (Edubuntu & Ubuntu) 6.06 VMware guests lose time (clock runs slowly) if :

- you are not using clock=pit
- you are not running the vmware-guest deamon
- you haven't added tools.syncTime = "TRUE" to your vmx file
- you've updated your kernel (which stops the vmware-guest deamon !)

You can fix this by

- add clock=pit to the kernel line in /boot/grub/menu.lst
- update-grub
- (get latest kernel headers)
- vmware-config.pl
- reboot

check that

- pstree -capl | grep guest

displays

- vmware-guestd,4555 --background /var/run/vmware-guestd.pid

Read more about you needn't shouldn't use NTP to solve these problems in the VMware white paper "Timekeeping in VMware Virtual Machines" hidden in [http://www.vmware.com/resources/techresources/](http://www.vmware.com/resources/techresources/ "vmware") as [http://www.vmware.com/resources/techresources/238](http://www.vmware.com/resources/techresources/238 "vmware")
