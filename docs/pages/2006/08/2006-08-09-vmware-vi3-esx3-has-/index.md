---
title: "VMware ESX 3 Virtual Infrastructure 3 has arrived"
date: 2006-08-09
categories: 
  - "vizz"
tags: 
  - "vmware"
---

vmsnap and vmrestore that was used to backup and restore vmwesx 2.5 (esx2.x) VMs & vmdk's have been replaced in vmwesx 3 with VMWVCB vcbMounter and vcbRestore

you will also need to get version 3 of vmbk.pl if you are using that to backup your VMs

\# vcbUtil -u root -p password -c ping # vcbUtil -u root -p password -c resourcepools # vcbUtil -u root -p password -c vmfolders

\# vcbVmName -u root -p password -s any:

\# vcbMounter -u root -p password -a powerstate:off -r /vmimages/off # vcbMounter -u root -p password -a moref:96 -r /vmimages/centos3 # vcbMounter -u root -p password -a name:centos4 -r /vmimages/centos4 # vcbMounter -u root -p password -a uuid:65D4EE45 -r /vmimages/centos5 # vcbMounter -u root -p password -a moref:16 -r /vmimages/rhel4

\# vcbRestore -u root -p password -s /vmimages/off/ -b overwrite

See

[http://pubs.vmware.com/vi301/backup/wwhelp/wwhimpl/common/html/wwhelp.htm?context=backup&file=vm\_bug\_appA.7.5.html](http://pubs.vmware.com/vi301/backup/wwhelp/wwhimpl/common/html/wwhelp.htm?context=backup&file=vm_bug_appA.7.5.html "vmware")

[http://www.vmware.com/products/beta/esx-vc/vcb-cos-esx30-usage.html](http://www.vmware.com/products/beta/esx-vc/vcb-cos-esx30-usage.html "vmware")

[http://www.petri.co.il/vmware-consolidated-backup-utilities.htm](http://www.petri.co.il/vmware-consolidated-backup-utilities.htm "petri")
