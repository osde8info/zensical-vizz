---
title: "VMware guests using GNU/Linux kernel 2.6.16+ and clock/clocksource"
date: 2007-09-18
categories: 
  - "vizz"
---

From kernel 2.6.16 the clock= command line option is deprecated and the following option should be used:

clocksource=acpi\_pm

The following option may be better suited to a Linux guest with kernel 2.6.21 or later and to VMware products such as VMware Workstation 6 that provide "VMware paravirtual kernel support":

clocksource=vmi-timer

Source [http://theether.net/kb/100039](http://theether.net/kb/100039 "clock")
