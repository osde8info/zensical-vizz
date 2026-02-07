---
title: "watchout @virtualbox nat networking is not the same as @vmware"
date: 2016-01-23
categories: 
  - "vizz"
tags: 
  - "nat"
  - "netadmin"
  - "networking"
  - "virtualbox"
  - "vmware"
  - "webdev"
---

WATCHOUT Oracle VirtualBox nat networking is not the same as VMware nat networking

VirtualBox 5.x default "built in" "hardcoded" NAT networking gives every VM the same IP 10.0.2.15 which will not let VMs talk to each other and VMs will also NOT work if you netadmin or sysadmin is using the 10.0.2.x subnet on your network

Apparently

_This separation maximizes security since by default virtual machines cannot talk to each other._

The documentation and network naming could be clearer BUT note in virtualbox if you want VMs to be able to talk to each other you must create your own "NAT Network" instead of using "NAT" network before creating VMs and assigning networks to them

- https://www.virtualbox.org/manual/ch06.html#networkingmodes
- https://www.virtualbox.org/manual/ch06.html#network\_nat
- https://www.virtualbox.org/manual/ch06.html#network\_nat\_service
- https://www.virtualbox.org/ticket/15061
