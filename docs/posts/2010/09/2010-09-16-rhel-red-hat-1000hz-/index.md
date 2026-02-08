---
title: "rhel red hat 1000Hz or 200Hz kernel"
date: 2010-09-16
categories: 
  - "vizz"
---

you can reduce the kernel clock rate in later versions of rhel 4 & 5 vmware vm guests from 1000Hz to 200Hz by adding divider=5 into the kernel start parameter line in your /boot/grub/menu.lst

for more info and other kernel start params such as clock= and clocksource= see

[http://vmware.com/red-hat-rhel-vm-guest-rtc-clock-issues](http://communities.vmware.com/blogs/vizz-info/2010/09/16/vmware-red-hat-rhel-vm-guest-rtc-clock-38-time-issues "vmware") [http://vmware.com/timekeeping-in-virtual-machines](http://blogs.vmware.com/management/2010/06/updated-timekeeping-in-vmware-virtual-machines-paper-available.html "vmware") [http://www.vmware.com/vmtn/resources/238](http://www.vmware.com/vmtn/resources/238 "vmware") [http://www.vmware.com/resources/techresources/238](http://www.vmware.com/resources/techresources/238 "vmware") [http://www.vmware.com/Timekeeping-In-VirtualMachines.pdf](http://www.vmware.com/files/pdf/Timekeeping-In-VirtualMachines.pdf "vmware") [http://kb.vmware.com/selfservice/externalId=1006427](http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1006427 "vmware")
