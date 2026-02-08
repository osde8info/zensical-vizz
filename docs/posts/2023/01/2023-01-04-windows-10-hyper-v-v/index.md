---
title: "windows 10 hyper-v vswitches for wsl are broken #devops #sysadmin"
date: 2023-01-04
categories: 
  - "vizz"
---

windows 10 hyper-v vswitches for wsl are broken (however they might work on windows 11)

```
The virtual machine or container JSON document is invalid.
Error code: Wsl/Service/CreateInstance/CreateVm/ConfigureNetworking/0x8037010d

[process exited with code 4294967295 (0xffffffff)]
```

https://github.com/microsoft/WSL/discussions/9227

Get-NetAdapter

```
Name                      InterfaceDescription                    ifIndex Status       MacAddress             LinkSpeed
---- -------------------- ------- ------ ---------- ---------
Appgate SDP               Appgate Tunnel                               20 Up                     100 Gbps
vEthernet (WSL)           Hyper-V Virtual Ethernet Adapter             61 Up           00- 10 Gbps
Ethernet                  Realtek PCIe GbE Family Controller            7 Disconnected 88- 0 bps
Ethernet 3                Zscaler Network Adapter 1.0.2.0               6 Disconnected 00- 100 Mbps
WiFi                      MediaTek Wi-Fi 6 MT7921 Wireless LAN...       5 Up           4C- 400 Mbps
Ethernet 2                Realtek PCIe GbE Family Controller #2         3 Disconnected 88- 0 bps
```

Get-NetAdapter

```
Name                      InterfaceDescription                    ifIndex Status       MacAddress             LinkSpeed
---- -------------------- ------- ------ ---------- ---------
Bluetooth Network Conn... Bluetooth Device (Personal Area Netw...      22 Disconnected 60         3 Mbps
vEthernet (MySwitch)      Hyper-V Virtual Ethernet Adapter #3          30 Disconnected F0          0 bps
Network Bridge            Microsoft Network Adapter Multiplexo...      41 Up           10       108 Mbps
vEthernet (Default Swi... Hyper-V Virtual Ethernet Adapter             51 Up           00        10 Gbps
WiFi                      Intel(R) Centrino(R) Advanced-N 6205         14 Up           10       108 Mbps
Ethernet 2                TAP-ProtonVPN Windows Adapter V9             10 Disconnected 00         1 Gbps
VirtualBox Host-Only N... VirtualBox Host-Only Ethernet Adapter         6 Up           0A         1 Gbps
vEthernet (MyBridge)      Hyper-V Virtual Ethernet Adapter #2          64 Up           10       108 Mbps
Ethernet                  Intel(R) 82579LM Gigabit Network Con...       3 Disconnected F0          0 bps
```

[![](https://vizz8info.wordpress.com/wp-content/uploads/2023/01/image.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2023/01/image.png)

[![](https://vizz8info.wordpress.com/wp-content/uploads/2023/01/image-1.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2023/01/image-1.png)
