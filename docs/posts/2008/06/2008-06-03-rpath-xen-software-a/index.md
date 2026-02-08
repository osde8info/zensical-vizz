---
title: "rPath Xen software appliance build options"
date: 2008-06-03
categories: 
  - "vizz"
tags: 
  - "rpath"
  - "software-appliances"
  - "vm-guest"
  - "xen"
---

[rPath](http://www.rpath.com/rbuilder/ "rpath") Xen software appliance virtual machine build options

Non Xen

- ~!domU, ~!xen

Xen domU

- domU, ~!group-dist.bothpae, ~!kernel.pae, ~kernel.smp, xen is: x86(mmx)

Xen domU+pae

- domU, ~!group-dist.bothpae, ~kernel.pae, ~kernel.smp, xen is: x86(mmx)
