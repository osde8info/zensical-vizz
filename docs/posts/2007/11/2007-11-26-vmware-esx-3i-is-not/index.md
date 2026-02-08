---
title: "VMware ESX 3i is not the same as VMware ESX 3"
date: 2007-11-26
categories: 
  - "vizz"
---

VMW ESX 3i is "functionally equivalent but the servers "local" service console has been removed. VMW ESX 3i uses only 32M so it can even be embedded in the hosts firmware.Since you can no longer login locally you must administer it remotely by using VMWVC, VMWVIC, remote command line or an agent that uses VIMAPI or CIM.

For example

- esxcfg-\* is replaced by vicfg-\*
- esxtop is replaced by resxtop
