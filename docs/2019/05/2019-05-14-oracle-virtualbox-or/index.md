---
title: "oracle virtualbox oracle linux 8 requires elfutils-libelf-devel"
date: 2019-05-14
categories: 
  - "vizz"
tags: 
  - "oracle-linux"
  - "virtualbox"
---

if you have oracle virtualbox and want to run virtualbox guest additions on a  centos 8, red hat 8 or oracle linux 8 vm  you will need to install kernel-devel and elfutils-libelf-devel before you run VBoxLinuxAdditions.run

```
# dnf install kernel-devel
# dnf install elfutils-libelf-devel

# ./VBoxLinuxAdditions.sh
```

see also

- https://linuxconfig.org/virtualbox-install-guest-additions-on-redhat-8
- https://www.linuxuprising.com/2019/01/manual-virtualbox-guest-additions.html
- https://community.oracle.com/tech/apps-infra/discussion/4270433/getting-virtualbox-guest-additions-working-with-oralce-linux-8
