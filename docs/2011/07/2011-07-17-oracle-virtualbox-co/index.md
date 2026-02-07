---
title: "oracle virtualbox copying hds doesnt work"
date: 2011-07-17
categories: 
  - "vizz"
---

On Windoz 7 64bit VBoxManage can be found in C:Program FilesOracleVirtualBox

Apparently one way to clone a vbo hd is

```
VBoxManage internalcommands sethduuid orac.vdi
UUID changed to: b534130a-XXXX-4e33-XXXX-9d64XXXX3ea2
```

```
but this does NOT work and you have use 'clonehd' instead !
```

UUID changed to: b534130a-XXXX-4e33-XXXX-9d64XXXX3ea2

VBoxManage clonehd orac.vdi orac2.vdi

0%...10%...20%...30%...40%...50%...60%...70%...80%...90%...100%

'VDI'. UUID: a1922153-9c96-4629-9eb9-c753e43664d8

See also

- [sadev.co.za/content/virtualbox-uuid-already-use](http://www.sadev.co.za/content/virtualbox-uuid-already-use)
- [forums.virtualbox.org/viewtopic.php?t=674](http://forums.virtualbox.org/viewtopic.php?t=674)
- [forums.virtualbox.org/viewtopic.php?p=33678](http://forums.virtualbox.org/viewtopic.php?p=33678)
- [giannistsakiris.com/index.php/how-to-change-the-uuid-vdi](http://www.giannistsakiris.com/index.php/2009/05/06/virtualbox-how-to-change-the-uuid-of-virtual-disk-vdi/)
- [semi-legitimate.com/blog/item/change-uuid-of-virtual-drive-vdi](http://semi-legitimate.com/blog/item/change-uuid-of-virtual-drive-vdi-in-virtualbox)

and

- [youtube.com/watch?gl=GB&v=y4mmQv-iHlI](http://www.youtube.com/watch?gl=GB&v=y4mmQv-iHlI)
