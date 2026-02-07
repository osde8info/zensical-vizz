---
title: "oracle virtualbox 7 oracle linux 7 &amp; 8 guest additions install"
date: 2022-12-22
categories: 
  - "vizz"
---

oracle virtualbox 7 oracle linux 7 8 guest additions install

# BOOT into non UEK kernel

choose normal kernel (NOT UEK kernel)

# install prereqs

```
dnf install gcc make kernel-devel
```

# elf

to prevent the `Cannot generate ORC metadata for CONFIG_UNWINDER_ORC=y` and / or `Could not find the X.Org or XFree86 Window System` errors

```
# cat /var/log/vboxadd-setup.log
Building the main Guest Additions 7.0.4 module for kernel 4.18.0-425.3.1.el8.x86_64.
Error building the module.  Build output follows.
make V=1 CONFIG_MODULE_SIG= CONFIG_MODULE_SIG_ALL= -C /lib/modules/4.18.0-425.3.1.el8.x86_64/build M=/tmp/vbox.0 SRCROOT=/tmp/vbox.0 -j1 modules
Makefile:993: *** "Cannot generate ORC metadata for CONFIG_UNWINDER_ORC=y, please install libelf-dev, libelf-devel or elfutils-libelf-devel".  Stop.
make: *** [/tmp/vbox.0/Makefile-footer.gmk:133: vboxguest] Error 2
Could not find the X.Org or XFree86 Window System, skipping.
modprobe vboxguest failed
```

you need to also install

```
dnf install elfutils-libelf-devel
```

# ? optional gui install ?

```
dnf groupinstall "xfce"
or
dnf groupinstall "server with gui"
```

then

```
reboot
```

# virtualbox install cd

click devices | insert guest additions

# mount cd

```
# blkid
/dev/sda1: UUID="720ebd3b-1271-4a1c-b9d6-73d1fa5d56f8" BLOCK_SIZE="512" TYPE="xfs" PARTUUID="58246022-01"
/dev/sda2: UUID="DrXngb-6Mk0-geTC-gGN2-EwL4-qZce-WM6ee1" TYPE="LVM2_member" PARTUUID="58246022-02"
/dev/sr0: BLOCK_SIZE="2048" UUID="2022-11-16-17-05-17-10" LABEL="VBox_GAs_7.0.4" TYPE="iso9660"

# mount /dev/sr0 /mnt
```

# run vbox guest additions install

```
cd /mnt
./VBoxLinuxAdditions.run
cd ~
eject
reboot
```
