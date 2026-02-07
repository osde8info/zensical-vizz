---
title: "Quiesce your live VMware VMs before you snapshot them"
date: 2007-11-28
categories: 
  - "vizz"
---

Make sure you quiesce any services such as Oracle 10g DB in your VMware VMs before you snap them:

- Install VMware Tools in your VM
- Create /usr/sbin/pre-freeze-script
- Create /usr/sbin/post-thaw-script

Use vcbMounter to snapshot your live VMware VM which will call /usr/sbin/pre-freeze-script just BEFORE creating the snap and /usr/sbin/post-thaw-script approx 1 second AFTER the delta/diff/redo file has been created BUT before the original VMDK has been been exported via vmkfstools.

\# cat /usr/sbin/pre-freeze-script

#!/bin/sh

#####################################

\# DO NOT modify this file directly as it will be overwritten the next # time the VMware Tools are installed. #####################################

echo frez$(date) >> /var/log/snap

\# cat /usr/sbin/post-thaw-script

#!/bin/sh

#####################################

\# DO NOT modify this file directly as it will be overwritten the next # time the VMware Tools are installed. #####################################

echo thaw$(date) >> /var/log/snap

\# tail /var/log/snap frezWed Nov 28 11:26:20 GMT 2007 thawWed Nov 28 11:26:21 GMT 2007
