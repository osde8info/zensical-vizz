---
title: "VMware ESX 2 v VMware ESX 3 live VM backups"
date: 2007-11-26
categories: 
  - "vizz"
tags: 
  - "vmware"
---

Basically during the VMware ESX two phase live backup process

ESX 2 uses .redo and .redo.redo "redo files" while

ESX 3 uses -0001-delta.vmdk and -0002-delta.vmdk "snapshots" In VMWESX 2 .redo and .redo.redo are used for live backups

Running

var.vmdk

Backup started

var.redo

var.vmdk

Backup completed (applying redo)

var.redo.redo

var.redo

var.vmdk

In VMWESX 3 snapshots -000001-delta.vmdk and -000002-delta.vmdk are used

Running VM

var-flat.vmdk

var.vmbk

Backup started

var-000001-delta.vmdk

var-000001.vmdk

Backup completed (applying, commiting, delete all, removing snapshots)

var-000002-delta.vmdk

var-000002.vmdk

var-000001-delta.vmdk

var-000001.vmdk

var-flat.vmdk

var.vmdk
