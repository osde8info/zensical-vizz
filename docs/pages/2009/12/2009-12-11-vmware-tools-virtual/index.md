---
title: "VMware Tools Virtual Shrink"
date: 2009-12-11
categories: 
  - "vizz"
tags: 
  - "tools"
---

If you've built a VMware VM but forgotten to turn off LVM and therefore cant use vmware virtual toolbox to shrink your disks you can still perform a virtual shrink by filling up your vm vmdks with 0's !

$ dd if=/dev/zero bs=40M count=40 of=1 $ dd if=/dev/zero bs=40M count=40 of=2 $ dd if=/dev/zero bs=40M count=40 of=3 $ dd if=/dev/zero bs=40M count=40 of=4 $ dd if=/dev/zero bs=40M count=40 of=5

etc etc

$ rm 1 2 3 4 5

This didnt affect the 11G of space used by my vm vmdk disks but it did reduce the tgz of the entire vm from 5.5G to 3.3G !
