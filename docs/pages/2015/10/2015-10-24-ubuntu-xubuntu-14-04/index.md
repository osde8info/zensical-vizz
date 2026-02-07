---
title: "ubuntu xubuntu 14.04.02 64-bit @oracle @virtualbox 5.0.8 64-bit on @intel T2390 only allows 32-bit vms ! why ?"
date: 2015-10-24
categories: 
  - "vizz"
tags: 
  - "32-bit"
  - "64-bit"
  - "intel"
  - "ubuntu"
  - "virtualbox"
---

ubuntu xubuntu 14.04.02 64bit @oracle @virtualbox 5.0.8 64bit on @intel T2390 only allows me to create 32bit vms ! why ?

```
$ uname -a 

Linux xubu14 3.16.0-51-generic #69~14.04.1-Ubuntu SMP Wed Oct 7 15:32:41 UTC 2015 x86_64 x86_64 x86_64 GNU/Linux

$ lsb_release -a 

No LSB modules are available.
Distributor ID:    Ubuntu
Description:    Ubuntu 14.04.3 LTS
Release:    14.04
Codename:    trusty

$ cat /proc/cpuinfo 

processor : 0
vendor_id : GenuineIntel
cpu family : 6
model : 15
model name : Intel(R) Pentium(R) Dual CPU T2390 @ 1.86GHz
stepping : 13
microcode : 0xa3
cpu MHz : 800.000
cache size : 1024 KB
physical id : 0
siblings : 2
core id : 0
cpu cores : 2
apicid : 0
initial apicid : 0
fpu : yes
fpu_exception : yes
cpuid level : 10
wp : yes
flags : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx lm constant_tsc arch_perfmon pebs bts rep_good nopl aperfmperf pni dtes64 monitor ds_cpl est tm2 ssse3 cx16 xtpr pdcm lahf_lm dtherm
bogomips : 3724.23
clflush size : 64
cache_alignment : 64
address sizes : 36 bits physical, 48 bits virtual
```
