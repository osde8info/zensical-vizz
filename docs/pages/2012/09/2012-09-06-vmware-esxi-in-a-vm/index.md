---
title: "VMware ESXi in a VM"
date: 2012-09-06
categories: 
  - "vizz"
tags: 
  - "esx"
  - "esxi"
  - "vm-in-a-vm"
  - "vmware"
---

Apparently you can run VMware VSphere ESXi inside a VMwareVM !

- You need to run VMware Player 4 or VMware Server 2 on the physical host since previous versions can't succesfully run ESX or ESXi in a VM.
- VM needs at least 1.5 GB of vmemory, 2 vCPUs and plenty of vSCSI disk space.

but you'll need to manually edit your VMX file to

```
guestOS = "vmkernel"
monitor_control.vt32 = "TRUE"
monitor_control.restrict_backdoor = "TRUE"
```

see [serverfault.com/how-to-run-vmware-esx-or-esxi-in-a-virtual-machine](http://serverfault.com/questions/28399/how-to-run-vmware-esx-or-esxi-in-a-virtual-machine)

and fix the clock

```
guestOS = "vmkernel"
timeTracker.apparentHz = 2376000000
timeTracker.apicBusHz = 66000000
```

see [kb.vmware.com/search.do?language=en\_US&cmd=displayKC&externalId=1030411](http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1030411)

[![esxi](http://farm9.staticflickr.com/8456/7948487500_3edd93d355_n.jpg)](http://www.flickr.com/photos/osde-info/7948487500/ "esxi by osde8info, on Flickr")

[![esxi2](http://farm9.staticflickr.com/8318/7948610088_e037967d2b_n.jpg)](http://www.flickr.com/photos/osde-info/7948610088/ "esxi2 by osde8info, on Flickr")
