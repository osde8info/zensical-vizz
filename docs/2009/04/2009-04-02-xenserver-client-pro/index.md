---
title: "XenServer client problems"
date: 2009-04-02
categories: 
  - "vizz"
tags: 
  - "xen"
  - "xen-server"
---

XenServer only provide a client as a .RPM or even worse a .MSI ! So if you'e running ed/x/ubuntu you'll need to install and run alien to convert the .RPM to .DEB and then run

\# dpkg -i xe-cli\_5.0.0-13193\_i386.deb.

When you try and run # xe you may then get the error

Please install the stunnel package or define the XE\_STUNNEL environment variable to point to the binary.

Time to install a CentOS VM to run XE i guess !
