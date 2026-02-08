---
title: "using #virtualbox to run a #bitnami #redmine #vmware vmdk #vm"
date: 2015-09-08
categories: 
  - "vizz"
tags: 
  - "bitnami"
  - "redmine"
  - "virtualbox"
  - "vm"
---

first off bitnami only provide vmware vm vmx & vmdk downloads and apparently you cant convert these to virtualbox disks BUT apparently virtualbox supports reading and writing to vmware vmdk disk files directly

what you need to do is

- build a vm without a disk (ignore warnings)
- download bitnami redmine vmware vm zip
- unzip files
- completely ignore .vmx
- copy \*.vmdk from unzip subdir into your virtualbox subdir
- reedit virtualbox vm and use existing sata disk and point it to .vmdk without the -s00n suffix
- ie bitnami-redmine-3.0.4-1-ubuntu-14.04.vmdk
- start virtualbox vm
- enjoy the virtualbox bitnami redmine gantt charts

see also

- https://wiki.bitnami.com/Virtual\_Appliances\_Quick\_Start\_Guide
- http://opendirective.net/blog/2014/07/on-converting-a-vm-from-vmware-to-virtualbox/
