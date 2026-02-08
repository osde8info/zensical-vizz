---
title: "Windows 10 Home WSL 2 &amp; Hyper-V"
date: 2022-12-19
categories: 
  - "vizz"
---

Windows Home WSL & Hyper V

_WSL 2 is available on all Desktop SKUs where WSL is available, including Windows 10 Home and Windows 11 Home._

_The newest version of WSL uses Hyper-V architecture to enable its virtualization. This architecture will be available in the '**Virtual Machine Platform'** optional component. This optional component will be available on all SKUs._

control panel install vm platform

control panel install wsl

check wsl version

```
C:\> wsl --version

WSL version: 1.0.3.0
Kernel version: 5.15.79.1
WSLg version: 1.0.47
MSRDC version: 1.2.3575
Direct3D version: 1.606.4
DXCore version: 10.0.25131.1002-220531-1700.rs-onecore-base2-hyp
Windows version: 10.0.19045.2364
```

even if it says 1 it might be 2

also check the hyperv vethernet wsl is running !

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/image-8.png?w=1022)](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/image-8.png)

refs

- https://learn.microsoft.com/en-us/windows/wsl/faq#does-wsl-2-use-hyper-v--will-it-be-available-on-windows-10-home-and-windows-11-home-
