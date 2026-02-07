---
title: "Red Hat RHEL, CentOS, OEL 4 &amp; 5 SAN filesystems go readonly !"
date: 2008-06-11
categories: 
  - "vizz"
tags: 
  - "centos"
  - "oracle-enterprise"
  - "red-hat"
  - "rhel"
  - "suse"
  - "ubuntu"
  - "vm"
  - "vmware"
---

Apparently there is a problem in the kernel used in Red Hat RHEL 4&5, CentOS 4&5, OEL 4&5, SUSE, Ubuntu 7 and other GNU/Linux distributions that causes EXT2 EXT3 filesystems that are residing on SANs to randomly go read-only !

However if you are using kernel 2.6.18-53.1.21+ or  2.6.22+ you should be ok !

See Red Hat

- [https://rhn.redhat.com/errata/RHSA-2007-0014.html](https://rhn.redhat.com/errata/RHSA-2007-0014.html "rhel")
- [http://kbase.redhat.com/faq/FAQ\_85\_10846.shtm](http://kbase.redhat.com/faq/FAQ_85_10846.shtm "rhel")
- [http://kbase.redhat.com/faq/FAQ\_85\_9610.shtm](http://kbase.redhat.com/faq/FAQ_85_9610.shtm "rhel")
- [https://bugzilla.redhat.com/show\_bug.cgi?id=213921](https://bugzilla.redhat.com/show_bug.cgi?id=213921 "rhel")

See VMware

- [http://communities.vmware.com/message/752884](http://communities.vmware.com/message/752884 "vmware")
- [http://kb.vmware.com/selfservice?externalId=1001778](http://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&externalId=1001778 "vmware")
- [http://kb.vmware.com/selfservice?externalId=51306](http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=51306 "vmware")
