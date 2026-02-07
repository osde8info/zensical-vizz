---
title: "AMD-V and Intel VT virtualisation extensions"
date: 2009-09-25
categories: 
  - "vizz"
tags: 
  - "kvm"
  - "xen"
---

[http://www.redhat.com/docs/en-US/Red\_Hat\_Enterprise\_Linux/5.4/html/Virtualization\_Guide](http://www.redhat.com/docs/en-US/Red_Hat_Enterprise_Linux/5.4/html/Virtualization_Guide/sect-Virtualization-Tips_and_tricks-Verifying_virtualization_extensions.html "red hat")

AMD-V or Intel VT virtualisation extensions are required for full KVM or Xen virtualisation.

Use $ cat /proc/cpuinfo to see what your CPU supports. You need either 'svm' or 'vmx' but note that some older Intel XEONs do not have this !
