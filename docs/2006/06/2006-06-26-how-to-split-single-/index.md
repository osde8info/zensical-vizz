---
title: "VMware vmware-vdiskmanager VMDK disk splitter"
date: 2006-06-26
categories: 
  - "vizz"
---

How to split single VMware (VI/ESX) VMDKs into multiple VMDKs (Player/Server) and change growable (Player/Server/Workstation) into pre-allocated (VI/ESX)

`$ vmware-vdiskmanager -r srcvmdk -t disktype dstvmdk`

Disk types:

0 : single growable virtual disk 1 : growable virtual disk split in 2Gb files 2 : preallocated virtual disk 3 : preallocated virtual disk split in 2Gb file

Finally don't forget to manually edit your .VMX file after you have converted your .VMDK

Here are some more examples

$ vmware-vdiskmanager -c -s 850Mb -a ide -t 0 myIdeDisk.vmdk $ vmware-vdiskmanager -d myDisk.vmdk $ vmware-vdiskmanager -r sourceDisk.vmdk -t 0 destinationDisk.vmdk $ vmware-vdiskmanager -x 36Gb myDisk.vmdk $ vmware-vdiskmanager -n sourceName.vmdk destinationName.vmdk
