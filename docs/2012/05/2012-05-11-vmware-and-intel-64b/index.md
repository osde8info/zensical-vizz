---
title: "VMware and Intel 64bit hosts &amp; guests"
date: 2012-05-11
categories: 
  - "vizz"
tags: 
  - "64-bit"
  - "intel"
  - "vmware"
  - "vt"
---

_VMware Workstation, Player, and Server require a 64-bit CPU to run a 64-bit guest operating system._

_Intel CPUs must have EM64T and VT support in the chip and in the BIOS. Intel EM64T CPUs do not have segmentation support in long mode. If the Intel EM64T CPU is VT-capable, it comes with hardware virtualization support (Intel's Virtualization Technology). This hardware virtualization support allows VMware to work around the lack of segmentation, making it possible to run 64-bit guest operating systems on Intel EM64T VT-capable CPUs._

_If the Intel site says that your CPU(s) support VT, but your VMware product says that your host does not support VT, you may have encountered an Intel chip erratum (possibly AW67, AV69, AX64, AY64, AZ69 or AAA70, depending on the CPU). The effect of this erratum is that some CPU features are reported incorrectly by the CPU. The only solution to this problem is to obtain an updated BIOS from your system vendor._

See

- [ark.intel.com/Products/VirtualizationTechnology](http://ark.intel.com/Products/VirtualizationTechnology)
- [kb.vmware.com/selfservice/microsites/search.do?externalId=1003945](http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1003945)
- [communities.vmware.com/docs/DOC-8978](http://communities.vmware.com/docs/DOC-8978)
- [my.vmware.com/processor\_check](https://my.vmware.com/web/vmware/details/processor_check_5_5_dt/dCpiQGhkYmRAZQ==)
