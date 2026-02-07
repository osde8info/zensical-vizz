---
title: "VMware Tools can&#039;t shrink ed/x/ubuntu 10.x ext4 partitions"
date: 2010-09-24
categories: 
  - "vizz"
tags: 
  - "tools"
  - "vmware"
---

Apparently it's a known issue that VMware tools toolbox cant shrink ed/x/ubuntu ext4 partitions. Until this is fixed by VMware one workaround from [http://www.insomnihack.com/?p=387](http://www.insomnihack.com/?p=387) suggests creating a large file of zeros then deleting it then using vmware-vdiskmanager on the command line.
