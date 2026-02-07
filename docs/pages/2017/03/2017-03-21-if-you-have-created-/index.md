---
title: "if you have created a ms windows domain cluster out of cloned vms you may need to run ntdsutil"
date: 2017-03-21
categories: 
  - "vizz"
tags: 
  - "adds"
  - "clone"
  - "domain"
  - "sid"
  - "vm"
  - "windoz"
---

if you have created a ms windows domains out of cloned (virtual box or vmware)  vms you may find you have duplicate SID security identifiers and you will need to run ntdsutil on your cloned servers before you add them to your domain to avoid getting this error:

_The operation failed because:_

_The attempt to join this computer to the "ADDS2012.HOME" domain failed._

_"The domain join cannot be completed because the SID of the domain you attempted to join was identical to the SID of this machine. This is a symptom of an improperly cloned operating system install.  You should run sysprep on this machine in order to generate a new machine SID. Please see http://go.microsoft.com/fwlink/?LinkId=168895 for more information."_

See

- https://support.microsoft.com/en-gb/help/816099/how-to-find-and-clean-up-duplicate-security-identifiers-with-ntdsutil-in-windows-server-2003
