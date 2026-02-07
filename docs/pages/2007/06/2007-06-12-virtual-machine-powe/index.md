---
title: "Virtual Machine Power &amp; Resource Saving"
date: 2007-06-12
categories: 
  - "vizz"
---

ARE you using Linux kernel version 2.6.21+ in your VMs ?

[http://osde-info.vox.com/library/post/intel-powertop.html](http://osde-info.vox.com/library/post/intel-powertop.html)

As of Linux kernel version 2.6.21, the kernel no longer has a fixed 1000Hz timer tick. This will (in theory) give a huge power savings because the CPU stays in low power mode for longer periods of time during system idle.

BETTER STILL are you using XEN VMs without any VGA card emulation !

[http://www.linuxpowertop.org/known.php](http://www.linuxpowertop.org/known.php)

The Intel graphics driver used to have a bug where it set up the hardware to generate an interrupt (called VBLANK) each time the screen finished refreshing (typically at 60Hz or 72Hz). In normal 2D mode, this interrupt isn't actually used. PowerTOP unveiled this bug and the current Intel graphics driver no longer has this behavior.
