---
title: "Howto use yum excludes to prevent kernel updates breaking VMware kernel modules"
date: 2008-02-15
categories: 
  - "vizz"
tags: 
  - "centos"
  - "oracle-enterprise"
  - "red-hat"
  - "vm-guest"
  - "vm-host"
  - "vmware"
---

If you are using CentOS 5 , Oracle Enterprise 5 or Red Hat Enterprise 5 as a VMware host or guest you can edit /etc/yum.conf and add a line

exclude=kernel\*

this should prevent yum updating your kernel and thus breaking vmware services modules in vmware server and vmware services modules in vmware guest tools

also see

[http://www.linuxmanpages.com/man5/yum.conf.5.php](http://www.linuxmanpages.com/man5/yum.conf.5.php "yum")

[http://linux.die.net/man/5/yum.conf](http://linux.die.net/man/5/yum.conf "yum")
