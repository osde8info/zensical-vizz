---
title: "XEN vm hwclock issues"
date: 2008-04-29
categories: 
  - "vizz"
tags: 
  - "clock"
  - "date"
  - "hardware"
  - "hwclock"
  - "sysadmin"
  - "time"
  - "vm-guest"
  - "xen"
---

It seems there are some issues with xen hwclock and centos and ubuntu xen vms !

- [http://howtoforge.com/debian\_sarge\_xen\_3.0.3\_p7](http://howtoforge.com/debian_sarge_xen_3.0.3_p7 "howto")
- [https://help.ubuntu.com/community/Xen](https://help.ubuntu.com/community/Xen "ubu")
- [http://wiki.xensource.com/xenwiki/CoolConfigurations](http://wiki.xensource.com/xenwiki/CoolConfigurations "xen")
- [http://jailtime.org/download:centos:v5.1?s=hwclock](http://jailtime.org/download:centos:v5.1?s=hwclock "jailtime")

You may find that installing # yum install system-config-date and using timeconfig instead might help
