---
title: "red hat 5.x 64bit &amp; vmware server 1.x"
date: 2010-09-03
categories: 
  - "vizz"
tags: 
  - "centos"
  - "enterprise-linux"
  - "oracle"
  - "server"
  - "vmware"
---

red hat enterprise linux 5.x 64bit with vmware server 1.x does not work out of the box ! since when you try and install it you may get the following error(s):

The correct version of one or more libraries needed to run VMware Server may be missing.

...

libX11.so.6 => not found

libXtst.so.6 => not found

libXext.so.6 => not found

libXt.so.6 => not found

libICE.so.6 => not found

libSM.so.6 => not found

libXrender.so.1 => not found

...

This program cannot tell for sure, but you may need to upgrade libc5 to glibc before you can run VMware Server.

and then when you try and enter your serial number you may get:

Please enter your 20-character serial number.

Type XXXXX-XXXXX-XXXXX-XXXXX or 'Enter' to cancel:

/usr/lib/vmware/bin/vmware-vmx:

error while loading shared libraries:

libX11.so.6:

cannot open shared object file:

No such file or directory

The serial number XXXXX-XXXXX-XXXXX-XXXXX is invalid.

this is because vmware server has been compiled against the 32bit X libraries which dont exist by default on a centos 64bit, oracle 64bit or red hat 64bit linux system so you'll need to install them manually using:

\# yum install libX libXtst libICE libSM

then re-run

\# vmware-config.pl
