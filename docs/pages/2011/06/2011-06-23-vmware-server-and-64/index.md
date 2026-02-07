---
title: "VMware Server and 64 bit guests"
date: 2011-06-23
categories: 
  - "vizz"
tags: 
  - "server"
  - "vmware"
---

Although VMware Server 2 should be able to support 64 bit guests it needs to be installed ontop of  a 64 bit OS on a 64 bit CPU  which has VT support.

For example a Dell PowerEdge 1800 with Intel(R) Xeon(TM) CPU 3.00GHz can only run 32 bit guests ! and if you try to install or run a 64 bit guest you'll get the error message:

```
Message on www: This host does not support VT.
You have configured this virtual machine to use a 64-bit guest operating system.
However, this host is not capable of running 64-bit virtual machines
or this virtual machine has 64-bit support disabled.
For more detailed information, see http://vmware.com/info?id=152
```
