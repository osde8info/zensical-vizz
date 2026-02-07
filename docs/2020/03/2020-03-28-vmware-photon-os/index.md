---
title: "VMware Photon OS™"
date: 2020-03-28
categories: 
  - "vizz"
tags: 
  - "arm64"
  - "distro"
  - "docker"
  - "lightweight"
  - "photon"
  - "vmware"
---

VMware Photon OS™ _is an open source, minimal Linux container host that is optimized for cloud-native applications, cloud platforms, and VMware infrastructure. Photon OS 3.0 introduces ARM64 support, installer improvements and updated packages._ 

- https://vmware.github.io/photon/
- https://github.com/vmware/photon/
- https://github.com/vmware/photon/wiki/Downloading-Photon-OS

You can choose to download an ISO or an OVA

The default user and password (root password) for the VMware Photon OS OVA is

```
user : root
password : changeme
```

How to reset VMware Photon OS root passwd

- https://vmware.github.io/photon/assets/files/html/3.0/photon\_troubleshoot/resetting-a-lost-root-password.html

```
e
linux ... rw init=/bin/bash
F10
```

```
# passwd 
New PASSWORD: ******
Retype PASSWORD: ******
# umount /
# reboot -f
```

How to import VMware Photon OS OVA

- https://github.com/vmware/photon/wiki/Running-Project-Photon-on-Fusion
- https://vmware.github.io/photon/assets/files/html/3.0/photon\_installation/importing\_ova\_for\_photon\_os\_3.0.html

How to build VMware Photon OS ISO from source

- https://vmware.github.io/photon/assets/files/html/3.0/photon\_installation/build-photon.html

How to enable VMware Photon OS SSH login

- https://vmware.github.io/photon/assets/files/html/3.0/photon\_troubleshoot/permitting-root-login-with-ssh.html
