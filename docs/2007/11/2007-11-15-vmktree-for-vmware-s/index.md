---
title: "vmktree for VMware Server"
date: 2007-11-15
categories: 
  - "vizz"
---

[vmktree](http://www.vmktree.org/ "vmktree") is a [free](http://www.vmktree.org/LICENSE) web tool that shows you the graphs of resource usage of [VMware ESX 2 Server](http://www.vmware.com/products/esx/), [VMware Server](http://www.vmware.com/products/server/) (on Linux) and GSX Server (on Linux). _On ESX vmktree depends on vmkusage that is part of the VMware-esx-perf package, a utility from VMware that is included in VMware ESX Server 2.1.x and 2.5.x. For **older** versions it must be downloaded from vmware. vmkusage does not exist on VI 2 ESX 3. vmktree generates graphs as needed while vmkusage generate static graphs every five minutes._

If you are using CentOS 4 as your VMware Server host OS you'll need to install RRDTOOL first

[http://dag.wieers.com/rpm/packages/rrdtool/](http://dag.wieers.com/rpm/packages/rrdtool/ "rrdtool")
