---
title: "ed/x/ubuntu and vmware tools &amp; vmware toolbox"
date: 2010-09-03
categories: 
  - "vizz"
tags: 
  - "player"
  - "tools"
  - "ubuntu"
  - "vmware"
  - "xubuntu"
---

If you have recently upgraded to the latest versions of ed/x/ubuntu (10.x) and the latest version of vmware player (3.1.1) you may experience the "good old" vmware tools & vmware toolbox "missing make", "missing gcc" or "missing kernel headers" errors !

These can normally be fixed by running

\# aptitude install bin-utils

\# aptitude install linux-headers-generic

before re-running

\# vmware-tools-distrib/vmware-install.pl

and

\# vmware-config-tools.pl
