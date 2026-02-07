---
title: "systemd-detect-virt detects if you are running in a vm"
date: 2018-02-08
categories: 
  - "vizz"
tags: 
  - "detection"
  - "identification"
  - "systemd"
---

https://www.freedesktop.org/software/systemd/man/systemd-detect-virt.html

_**systemd-detect-virt** detects execution in a virtualized environment. It identifies the virtualization technology and can distinguish full machine virtualization from container virtualization. `systemd-detect-virt` exits with a return value of 0 (success) if a virtualization technology is detected, and non-zero (error) otherwise._

```
$ systemd-detect-virt
vmware
```

 

| VM | `qemu` | QEMU software virtualization, without KVM |
| :-- | :-- | :-- |
| `kvm` | Linux KVM kernel virtual machine, with whatever software, except Oracle Virtualbox |
| `zvm` | s390 z/VM |
| `vmware` | VMware Workstation or Server, and related products |
| `microsoft` | Hyper-V, also known as Viridian or Windows Server Virtualization |
| `oracle` | Oracle VM VirtualBox (historically marketed by innotek and Sun Microsystems), for legacy and KVM hypervisor |
| `xen` | Xen hypervisor (only domU, not dom0) |
| `bochs` | Bochs Emulator |
| `uml` | User-mode Linux |
| `parallels` | Parallels Desktop, Parallels Server |
| `bhyve` | bhyve, FreeBSD hypervisor |
