---
title: "HOWTO Disable VMware Server 2 autostart &amp; mgmt"
date: 2010-10-22
categories: 
  - "vizz"
tags: 
  - "server"
  - "vmware"
---

By default the VMware Server 2 file /etc/rc.d/init.d/vmware starts and stops all three vmware services (core, mgmt, autostart) so if you never want autostart to run you can comment out all the "service\_vmware\_autostart" lines !
