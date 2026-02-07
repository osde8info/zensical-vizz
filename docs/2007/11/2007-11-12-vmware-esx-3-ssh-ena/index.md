---
title: "VMware ESX 3 ssh enable"
date: 2007-11-12
categories: 
  - "vizz"
---

\# vi sshd\_config

PermitRootLogin yes # esxcfg-firewall --allowIncoming

\# esxcfg-firewall --allowOutgoing
