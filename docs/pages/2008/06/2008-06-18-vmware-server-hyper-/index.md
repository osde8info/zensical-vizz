---
title: "VMWare Server, hyper threading CPUs and the SMP kernel"
date: 2008-06-18
categories: 
  - "vizz"
tags: 
  - "centos"
  - "hyper-threading"
  - "kernel"
  - "smp"
  - "vm"
  - "vmware"
  - "vmwsvr"
---

Just noticed an interesting quirk with VMWare Server and hyper threading CPUs

I told my VM to use 1 CPU but CentOS 4 install detected the underlying hardware CPU had hyper threading so installed the SMP kernel !

Linux localhost.localdomain 2.6.9-67.0.15.ELsmp #1 SMP Thu May 8 10:52:19 EDT 2008 i686 i686 i386 GNU/Linux

as opposed to creating a VM where underlying hardware didn't have hyper threading where CentOS 4 install just installed the basic kernel !

Linux localhost.localdomain 2.6.9-67.0.15.EL #1 Thu May 8 10:39:19 EDT 2008 i686 i686 i386 GNU/Linux
