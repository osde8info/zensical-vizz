---
title: "vmware workstation player vm backup and export"
date: 2018-02-08
categories: 
  - "vizz"
tags: 
  - "backup"
  - "export"
  - "player"
  - "save"
  - "vm"
  - "vmware"
---

in the latest version of vmware workstation player (14) you can no longer backup a vm or export a vm from the gui instead you need to run ovtool from the command line

```
C:\> "C:\Program Files (x86)\VMware\VMware Player\OVFTool\ovftool.exe" -h
```

eg

```
C:\> ovftool.exe path-to-your-vmx path-to-your-ova-file-or-ovf-dir
```

you can specify target type instead of using file suffix ie OVA, OVF

```
C:\> ovftool.exe --targettype OVA path-to-your-vmx path-to-your-ova-file
```

see also

- https://www.vmware.com/support/pubs/player\_pubs.html
- https://docs.vmware.com/en/VMware-Workstation-Player/index.html
- https://docs.vmware.com/en/VMware-Workstation-Player/12.0/workstation-player-12-windows-user-guide.pdf
- https://www.vmware.com/support/developer/ovf/
- https://www.vmware.com/support/developer/ovf/ovf420/ovftool-420-userguide.pdf
