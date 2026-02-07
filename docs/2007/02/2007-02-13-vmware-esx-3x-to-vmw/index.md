---
title: "VMware ESX 3.x VM to VMware Server 1.0.1VM"
date: 2007-02-13
categories: 
  - "vizz"
---

There are two techniques you can use to migrate a VMWESX 3.x virtual machine to VMWSVR.

1. Create a new VMWSVR VM and point its disks to a copy of a snap of your ESX VM disks
2. Copy entire snap (inc .vmx file) to VMWSVR then delete "catalog" file and rename .vmdk file(s)
