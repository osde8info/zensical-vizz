---
title: "VMware VI ESX VCB backup commands"
date: 2007-11-15
categories: 
  - "vizz"
tags: 
  - "vmware"
---

You can put your default VCHOST, USERNAME, PASSWORD in /etc/vmware/backuptools if you prefer

VMFS folders $ vcbUtil -h localhost -u root -p password -s vmfolders

VMs

$ vcbVmName -h localhost -u root -p password -s any:

Backup

$ vcbMounter -h localhost -u root -p password -a uuid:myvm -r /vmimages/vmbk

Restore (to same location)

$ vcbRestore -h localhost -u root -p password -a uuid:myvm -r /vmimages/vmbk

Restore (to different location)

$ vcbRestore -h localhost -u root -p password -s /vmimages/vmbk/myvm -a /vmimages/my-alt-catalog
