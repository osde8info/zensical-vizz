---
title: "how to ssh into a vbox vm or m$ wsl instance on a remote (ie not localhost) host"
date: 2023-01-04
categories: 
  - "vizz"
---

how to ssh into a vbox vm or m$ wsl instance on a remote (not local) host

## 1 vbox (the EASYWAY)

create vbox vm on (remote host) with BRIDGED network  
ssh to IP of remote VM

## 2 wsl firewall & proxy (the HARDWAY)

create a firewall rule to allow ssh to your (remote) host (22)  
get IP of wsl instance  
create a netsh proxy rule to proxy ssh tcp into your wsl instance  
ssh to IP of remote HOST

## 3 windows 11 wsl bridged network

https://github.com/microsoft/WSL/discussions/9227

## 2a)

use PS1 cmds

```
Get-NetFirewallPortFilterNew-NetFireWallRule -DisplayName 'ALLOW SSH' -Direction Inbound -LocalPort 22 -Action Allow -Protocol TCPGet-NetFirewallPortFilter
```

or NETSH cmds

```
netsh advfirewall show all
netsh advfirewall firewall add rule name="ALLOW SSH" dir=in action=allow protocol=TCP localport=22
netsh advfirewall show all
```

## 2b)

WSLIP = $(wsl hostname -I) ie 192.168.XXX.YYY

## 2c)

```
netsh interface portproxy show v4tov4
netsh interface portproxy add v4tov4 listenaddress=0.0.0.0 listenport=22 connectaddress=[WSLIP]
netsh interface portproxy show v4tov4
```

## FW SHOW

```
Name : {87935fe6-0809-4bdb-ac11-01c836f59ee0}DisplayName : ALLOW SSHDescription :DisplayGroup :Group :Enabled : TrueProfile : AnyPlatform : {}Direction : InboundAction : AllowEdgeTraversalPolicy : BlockLooseSourceMapping : FalseLocalOnlyMapping : FalseOwner :PrimaryStatus : OKStatus : The rule was parsed successfully from the store. (65536)EnforcementStatus : NotApplicablePolicyStoreSource : PersistentStorePolicyStoreSourceType : LocalRemoteDynamicKeywordAddresses :
```

FW SHOW

```
Rule Name: ALLOW SSH
Enabled: Yes
Direction: In
Profiles: Domain,Private,Public
Grouping:
LocalIP: Any
RemoteIP: Any
Protocol: TCP
LocalPort: 22
RemotePort: Any
Edge traversal: No
Action: Allow
```

FW SHOW

Protocol : TCP  
LocalPort : 22  
RemotePort : Any  
IcmpType : Any  
DynamicTarget : Any

## PX SHOW

Listen on ipv4: Connect to ipv4:

Address Port Address Port  
\--------------- ---------- --------------- ---------- 
0.0.0.0 22 172.23.XXX.YYY 22

## 2d)

ssh you@IP of remote HOST

## notes

"netsh firewall" is deprecated use "netsh advfirewall firewall" instead.

## refs

- https://www.hanselman.com/blog/how-to-ssh-into-wsl2-on-windows-10-from-an-external-machine

- https://github.com/microsoft/WSL/issues/4150?WT.mc\_id=-blog-scottha

- https://gist.github.com/daehahn/497fa04c0156b1a762c70ff3f9f7edae?WT.mc\_id=-blog-scottha

- https://learn.microsoft.com/en-us/windows-server/networking/technologies/netsh/netsh-interface-portproxy#add-v4tov4

- https://go.microsoft.com/fwlink/?linkid=121488
