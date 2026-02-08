---
title: "VMware guest slow fast clock timer fix"
date: 2006-12-12
categories: 
  - "vizz"
tags: 
  - "vmware"
---

If your VMware Player / Server / Workstation / ESX CentOS, gNewSense, RHEL or Ed/X/Ubuntu guest clock timer is running too slowly you may need to add "clock=pit" to your kernel command line !

**If you are running a CentOS 4 or Red Hat RHEL 4 guest :**

\# vi /boot/grub/menu.lst

kernel /vmlinuz-2.6.9-22.EL ro root=LABEL=/ rhgb quiet **clock=pit**

**If you are running a gNewSense 1.x.y or Ubuntu 6.x.y guest :** \# vi /boot/grub/menu.lst

and add "clock=pit" to the "defoptions" "comment"

\# defoptions=quiet splash clock=pit

run

\# update-grub

then

\# cat menu.lst

and check kernel line now contains "clock=pit"

kernel /boot/vmlinuz-2.6.15-28-686 root=/dev/sda1 ro quiet splash clock=pit
