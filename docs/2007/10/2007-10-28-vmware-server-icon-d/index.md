---
title: "VMware Server icon dies"
date: 2007-10-28
categories: 
  - "vizz"
---

If your VMware Server icon dies as soon as you click on it try running it from the command line instead \[$ vmware\] and you might get a more detailed error message such as:

"VMware isinstalled, but it has not been (correctly) configured for this system. To (re-)configure it, invoke the following command:/usr/bin/vmware-config.pl."

this may mean you've recently autoupdated/aptituded/up2dated or yummed the kernel on your host OS so you need to re-run /usr/bin/vmware-config.pl
