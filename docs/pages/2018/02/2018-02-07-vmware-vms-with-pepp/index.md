---
title: "vmware vms with peppermint 8 dont work with open-vm-tools"
date: 2018-02-07
categories: 
  - "vizz"
tags: 
  - "open-vm-tools"
  - "peppermint"
  - "vmware"
---

in a peppermint 8 gnu/linux vmware vm open-vm-tools and open-vm-tools-desktop do not work so when installing peppermint 8 into a vmware vm do not use open-vm-tools (the screen never resizes)

use VMware Workstation Player | Manage | Install VMware tools instead and when you run vmware-config-tools.pl say NO to all the questions ESPECIALLY

```
Would you like to enable VMware automatic kernel modules? NO
```

See also

- https://forum.peppermintos.com/index.php?topic=6562
