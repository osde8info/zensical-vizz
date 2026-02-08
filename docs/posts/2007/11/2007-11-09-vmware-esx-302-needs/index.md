---
title: "VMware ESX 3.0.2 needs EM64T and VT to run 64-bit guests"
date: 2007-11-09
categories: 
  - "vizz"
tags: 
  - "vm-host"
  - "vmware"
---

It would appear that VMware ESX 3.0.2 needs your CPU to have EM64T and VT features and that Execute Disable is enabled in the BIOS (e.g. an Intel Xeon E5300 X5365) to run 64-bit VMware guest virtual machines !

Here are some other Red Hat RHEL 64 bit guest issues you might see

http://kb.vmware.com/selfservice/microsites/search.do?language=en\_US&cmd=displayKC&externalId=2087

http://kb.vmware.com/selfservice/microsites/search.do?language=en\_US&cmd=displayKC&externalId=2260

http://kb.vmware.com/selfservice/microsites/search.do?language=en\_US&cmd=displayKC&externalId=2263

http://kb.vmware.com/selfservice/microsites/search.do?language=en\_US&cmd=displayKC&externalId=10147

http://kb.vmware.com/selfservice/microsites/search.do?language=en\_US&cmd=displayKC&externalId=2229
