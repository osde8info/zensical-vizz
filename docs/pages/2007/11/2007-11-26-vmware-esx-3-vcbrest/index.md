---
title: "VMware ESX 3 vcbRestore quick restore"
date: 2007-11-26
categories: 
  - "vizz"
tags: 
  - "vmware"
---

After backing up a VMWESX VM with vcbMounter you can use vcbRestore to perform a quick restore on another ESX server

Edit the catalog file

- change SOURCE hostname to DEST hostname
- check the same "resource pool" exists on DEST host (if not change it so it does)

for example

- host=myserver.mydomain

- resourcepool= "/ha-folder-root/ha-datacenter/host/myserver.mydomain/Resources"
