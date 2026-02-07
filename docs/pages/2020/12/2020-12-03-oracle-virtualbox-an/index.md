---
title: "Oracle VirtualBox and VMware Player network modes confusion #virtualbox #vmwareplayer #netadmin #sysadmin"
date: 2020-12-03
categories: 
  - "vizz"
---

do not get confused between Oracle VirtualBox and VMware Player network modes

the default Oracle VirtualBox NAT (is unlike the default VMware NAT network) and breaks VM 2 VM comms by giving each VM the same IP ADDRESS

the only Oracle VirtualBox network modes that allow VMs to talk to VMs AND the outside world are BRIDGED and NATNETWORK (which is diff to NAT and NATNETWORK is called/renamed NATSERVICE a few paragraphs later)

> 6.2. Introduction to Networking Modes  
> Each of the networking adapters can be separately configured to operate in one of the following modes:

> Not attached. In this mode, Oracle VM VirtualBox reports to the guest that a network card is present, but that there is no connection. This is as if no Ethernet cable was plugged into the card. Using this mode, it is possible to pull the virtual Ethernet cable and disrupt the connection, which can be useful to inform a guest operating system that no network connection is available and enforce a reconfiguration.
> 
> Network Address Translation (NAT). If all you want is to browse the Web, download files, and view email inside the guest, then this default mode should be sufficient for you, and you can skip the rest of this section. Please note that there are certain limitations when using Windows file sharing. See Section 6.3.3, “NAT Limitations”.
> 
> NAT Network. A NAT network is a type of internal network that allows outbound connections. See Section 6.4, “Network Address Translation Service”.
> 
> Bridged networking. This is for more advanced networking needs, such as network simulations and running servers in a guest. When enabled, Oracle VM VirtualBox connects to one of your installed network cards and exchanges network packets directly, circumventing your host operating system's network stack.
> 
> Internal networking. This can be used to create a different kind of software-based network which is visible to selected virtual machines, but not to applications running on the host or to the outside world.
> 
> Host-only networking. This can be used to create a network containing the host and a set of virtual machines, without the need for the host's physical network interface. Instead, a virtual network interface, similar to a loopback interface, is created on the host, providing connectivity among virtual machines and the host.
> 
> Generic networking. Rarely used modes which share the same generic network interface, by allowing the user to select a driver which can be included with Oracle VM VirtualBox or be distributed in an extension pack.
