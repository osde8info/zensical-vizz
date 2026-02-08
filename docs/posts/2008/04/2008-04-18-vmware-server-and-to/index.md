---
title: "VMware Server and top !"
date: 2008-04-18
categories: 
  - "vizz"
tags: 
  - "host"
  - "monitoring"
  - "server"
  - "sysadmin"
  - "top"
  - "vmware"
---

Have you ever wondered which VM is which when looking at top```
top - 11:58:00 up 56 days,  1:08,  1 user,  load average: 0.57, 0.59, 0.96
Tasks:  88 total,   2 running,  86 sleeping,   0 stopped,   0 zombie
Cpu(s):  1.8%us, 12.1%sy,  0.0%ni, 86.1%id,  0.0%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:   1553968k total,  1517840k used,    36128k free,     4500k buffers
Swap:  2040244k total,   107652k used,  1932592k free,  1282832k cachedPID USER      PR  NI  VIRT  RES  SHR S %CPU %MEM    TIME+  COMMAND

12387 user       5 -10  793m 533m 479m S  1.4 35.1  83:56.98 vmware-vmx
12310 user  5 -10  743m 510m 497m S  8.9 33.7 277:42.39 vmware-vmx
3368 user       5 -10  447m 182m 168m S  2.1 12.0   3214:21 vmware-vmx
2537 root      15   0 19040 4728 1572 S  0.0  0.3  95:12.36 vmware-serverd

```

well just make your xterm screen wider run "top" and press "c"```
top - 11:58:10 up 56 days,  1:09,  1 user,  load average: 0.56, 0.59, 0.96
Tasks:  88 total,   1 running,  87 sleeping,   0 stopped,   0 zombie
Cpu(s):  1.2%us, 12.6%sy,  0.0%ni, 86.1%id,  0.0%wa,  0.1%hi,  0.0%si,  0.0%st
Mem:   1553968k total,  1517964k used,    36004k free,     4516k buffers
Swap:  2040244k total,   107652k used,  1932592k free,  1282888k cached

PID USER      PR  NI  VIRT  RES  SHR S %CPU %MEM    TIME+  COMMAND
12387 user       5 -10  793m 533m 479m S  1.4 35.1  83:57.12 /usr/lib/vmware/bin/vmware-vmx -C /vmfs/w2k8/w2k8.vmx -@ ""
12310 user       5 -10  743m 510m 497m S  8.3 33.7 277:43.21 /usr/lib/vmware/bin/vmware-vmx -C /vmfs/rhyth/rhyth.vmx -@ ""
3368 user       5 -10  447m 182m 168m S  3.2 12.0   3214:21 /usr/lib/vmware/bin/vmware-vmx -C /vmfs/redmine-0.5/JumpBox.vmx
2537 root      15   0 19040 4728 1572 S  0.3  0.3  95:12.39 /usr/sbin/vmware-serverd -s -d

```
