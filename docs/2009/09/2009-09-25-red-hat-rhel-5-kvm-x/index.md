---
title: "Red Hat RHEL 5 KVM &amp; Xen unconfusion !"
date: 2009-09-25
categories: 
  - "vizz"
tags: 
  - "kvm"
  - "red-hat"
  - "rhel"
  - "xen"
---

[Red Hat Enterprise Linux 5.4](http://www.redhat.com/docs/en-US/Red_Hat_Enterprise_Linux/5.4/html/Release_Notes/ "red hat kvm xen")

_now includes full support for the Kernel-based Virtual Machine (KVM) hypervisor on x86\_64 based architectures. KVM is integrated into the Linux kernel, providing a virtualization platform that takes advantage of the stability, features, and hardware support inherent in Red Hat Enterprise Linux._

Note _Xen is the default hypervisor that is shipped with Red Hat Enterprise Linux. As such all configuration defaults are tailored for use with the Xen hypervisor. For details on configuring a system for KVM, please refer to the Virtualization Guide._ Important _Xen based virtualization is fully supported. However, Xen-based virtualization requires a different version of the kernel to function. The KVM hypervisor can only be used with the regular (non-Xen) kernel._ Warning _While Xen and KVM may be installed on the same system, the default networking configuration for these are different. Users are strongly recommended to only install one hypervisor on a system._
