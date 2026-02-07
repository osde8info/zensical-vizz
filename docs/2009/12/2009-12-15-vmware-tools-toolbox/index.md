---
title: "VMware tools toolbox XFCE startup problem"
date: 2009-12-15
categories: 
  - "vizz"
tags: 
  - "tools"
---

If your Xubuntu 8.x/9.x (XFCE) VM keeps logging you out on startup it may be a problem with your XFCE config startup or VMware tools toolbox startup settings.

So just reboot your VM into single user mode or login as root (only if you've pre/re/enabled root account login) and goto the users directory that has the problem and :

```
# cd ~user-with-problem
```

```
# mv .config .old
```

```
# logout
```

Now you should be able to re-login as then problem user !

However they will have lost all their XFCE X11 X settings but you can now :

```
$ diff -qr .config .old
```

to investigate the XFCE or VMware setting that was causing the problem !

You can also check your .xsession-errors file(s) to see if you're getting:

```
vmware-user: could not open /proc/fs/vmblock/dev
```

in which case you could try and re-run vmware-config-tools.pl and reboot to fix !
