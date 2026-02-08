---
title: "AsteriskNow &amp; TrixBox under VMware fusion"
date: 2009-04-21
categories: 
  - "vizz"
tags: 
  - "fusion"
---

Howto install AsteriskNow & TrixBox as MAC OS/X VMware fusion virtual machines / software appliances

First DO NOT choose RedHat at your guest OS or your VOIP PBX VM wont recognise the VMware SCSI disk ! You must choose RHEL5 as your guest OS so that scsi0.virtualDev = "lsilogic" is added to your guest VMX file. There's the danger of Wizards for you !

Both AsteriskNow and Trixbox are based on CentOS 5 with linux kernel 2.6.18.

AsteriskNow has a GUI installer so you can replace the default LVM partitions with standard linux partitions if you wish.

TrixBox has a TEXT installer.
