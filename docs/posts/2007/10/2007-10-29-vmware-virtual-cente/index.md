---
title: "VMware Virtual Center 1.4.1 and VMware Server"
date: 2007-10-29
categories: 
  - "vizz"
tags: 
  - "vmware"
---

Here are some VMware Virtual Center 1.4.1 (VMWVC) with VMware Server (VMWSVR) demo / 30 day eval tips:

- Don't be put off by the VMWVC min spec of P4 & 2G RAM - it works (for demo/eval purposes) on a PIII with only 256M RAM !
- Make sure you install VMWSVR on CentOS/Red Hat/Oracle instead of Debi/Ubun (so you can connect as root from VMWVC to VMWSVR)
- Make sure you install the VMWSVR MUI Console
- Remember you first need to add a Farm Group and then a Farm before you can do File | New | Add Host and then finally add any optional Virtual Machine Groups
- Don't run the Server Console against the VMWSVR you wish to manage with VMWVC

![vmware vc and server](http://farm3.static.flickr.com/2111/1800580448_3ef2391713_m.jpg "vmware vc and server")
