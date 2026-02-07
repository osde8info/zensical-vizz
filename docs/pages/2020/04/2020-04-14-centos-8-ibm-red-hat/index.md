---
title: "CentOS 8 &amp; IBM Red Hat 8 QEMU &amp; KVM"
date: 2020-04-14
categories: 
  - "vizz"
tags: 
  - "centos"
  - "ibmredhat"
  - "kvm"
  - "qemu"
---

CentOS 8 & IBM Red Hat 8 support QEMU & KVM

```
# yum groupinstall "Virtualization Host"
# yum install virt-install
# yum install virt-manager
# yum install libvirt-nss
# systemctl enable --now libvirtd
```

however note that IBM Red Hat say

_while QEMU is an essential component of the architecture, it is not intended to be used directly on RHEL 8 systems, due to security concerns. Therefore, using `qemu-*` commands is not supported by Red Hat, and it is highly recommended to interact with QEMU using libvirt._

so on centos 8 and ibm red hat 8 instead of qemu-\* use these commands

```
$ virt-host-validate
$ virt-install
$ virt-manager
$ virt-viewer
$ virsh
```

See also

- https://www.qemu.org/docs/master/system/quickstart.html
- https://wiki.centos.org/HowTos/KVM
- https://linuxconfig.org/redhat-8-kvm-install-guide
- https://linuxhint.com/kvm\_qemu\_centos8\_install/
- https://www.itzgeek.com/how-tos/linux/centos-how-tos/install-kvm-qemu-on-centos-7-rhel-7.html

and red hat developers also can refer to

- https://access.redhat.com/documentation/en-us/red\_hat\_enterprise\_linux/8/html/configuring\_and\_managing\_virtualization/virtualization-in-rhel-8-an-overview\_configuring-and-managing-virtualization#con\_tools-and-interfaces-for-virtualization-management-in-RHEl8\_virt-overview
