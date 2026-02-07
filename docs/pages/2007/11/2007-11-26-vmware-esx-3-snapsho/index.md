---
title: "VMware ESX 3 snapshots"
date: 2007-11-26
categories: 
  - "vizz"
---

Here's a CentOS 4 VM with 4 snapshots, in each snapshot I added a 40M file and in two of the snapshots i snapped the memeory as well.

Note a memory snapshot file is ALWAYS created if it doesn't contain anything !

The .VMSD contains a snapshot definition !

![http://farm3.static.flickr.com/2225/2065721033_1fae81b809.jpg](http://farm3.static.flickr.com/2225/2065721033_1fae81b809.jpg "http://farm3.static.flickr.com/2225/2065721033_1fae81b809.jpg")

\-rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â  8.0G Nov 26 17:26 cent4-flat.vmdk -rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  334 Nov 21 12:39 cent4.vmdk

\-rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â  1.4K Nov 26 17:31 cent4.vmsd

\-rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  48M Nov 26 17:28 cent4-000001-delta.vmdk -rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  219 Nov 26 17:27 cent4-000001.vmdk -rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  18K Nov 26 17:27 cent4-Snapshot1.vmsn

\-rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  48M Nov 26 17:29 cent4-000002-delta.vmdk -rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  226 Nov 26 17:28 cent4-000002.vmdk -rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â  257M Nov 26 17:28 cent4-Snapshot2.vmsn

\-rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  48M Nov 26 17:31 cent4-000003-delta.vmdk -rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  226 Nov 26 17:29 cent4-000003.vmdk -rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â  257M Nov 26 17:29 cent4-Snapshot3.vmsn

\-rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  16M Nov 26 17:31 cent4-000004-delta.vmdk -rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  226 Nov 26 17:31 cent4-000004.vmdk -rw-------Â Â Â  1 rootÂ Â Â Â  rootÂ Â Â Â Â Â Â Â Â  18K Nov 26 17:31 cent4-Snapshot4.vmsn
