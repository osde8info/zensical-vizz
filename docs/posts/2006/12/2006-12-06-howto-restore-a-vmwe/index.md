---
title: "HOWTO : Restore a vmwesx 2.5 vm &amp; vmdk onto vmwsvr 1.0.0"
date: 2006-12-06
categories: 
  - "vizz"
---
## Steps

1. snap vm on esx
1. copy/scp snap files to vmwsvr
1. edit vm.vmx

replace  

```html
<table>
<tbody><tr><td valign="top" bgcolor="#ffffff" align="left"><pre>scsi0.virtualDev = <font color="red">"vmxlsilogic"</font>
with scsi0.virtualDev = <font color="red">"lsilogic"</font></pre></td></tr></tbody>
</table>  
```

or replace  

```html
<table>
<tbody><tr><td valign="top" bgcolor="#ffffff" align="left"><pre>scsi0.virtualDev = <font color="red">"vmxbuslogic"</font>
with scsi0.virtualDev = <font color="red">"buslogic"</font></pre></td></tr></tbody>
</table>  
```

1. edit vm.vmx remove any vdisk: prefix from reference to vmdk
1. browse and add vm to vmwsvr inventory
1. power on vm
