---
title: "VMware Tools in Debian 4.0 (xorg 7.1) and Ubuntu 7.04 (xorg 7.2) guests"
date: 2007-05-08
categories: 
  - "vizz"
---

In both VMware Server 1.0.3 and VMware Workstation the vm mouse does not function properly in GNU/Linux guests that use xorg 7.1 or higher

```
# aptitude install xserver-xorg-input-vmmouse
and
# vi /etc/X11/xorg.conf
```

and change "mouse" to "vmmouse"

See the [VMware KB](http://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&docType=kc&externalId=5739104&sliceId=2&docTypeID=DT_KB_1_1&dialogID=2226328&stateId=0%200%202224503 "VMware KB")
