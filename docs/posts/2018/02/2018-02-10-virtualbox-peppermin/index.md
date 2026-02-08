---
title: "virtualbox peppermint vm installs require you to run ./VBoxLinuxAdditions.run twice"
date: 2018-02-10
categories: 
  - "vizz"
tags: 
  - "peppermint"
  - "virtualbox"
---

virtualbox peppermint vm installs require you to run ./VBoxLinuxAdditions.run twice

 

run VBoxLinuxAdditions.run it fails with the error "modprobe vboxsf failed" reboot

run VBoxLinuxAdditions.run it fails it works

Code:

```
# ./VBoxLinuxAdditions.run 
Verifying archive integrity... All good.
Uncompressing VirtualBox 5.2.6 Guest Additions for Linux........
VirtualBox Guest Additions installer
Copying additional installer modules ...
Installing additional modules ...
VirtualBox Guest Additions: Building the VirtualBox Guest Additions kernel modules.
VirtualBox Guest Additions: Running kernel modules will not be replaced until the system is restarted
VirtualBox Guest Additions: Starting.
VirtualBox Guest Additions: modprobe vboxsf failed
```

Code:  `# ./VBoxLinuxAdditions.run Verifying archive integrity... All good. Uncompressing VirtualBox 5.2.6 Guest Additions for Linux........ VirtualBox Guest Additions installer Removing installed version 5.2.6 of VirtualBox Guest Additions... Copying additional installer modules ... Installing additional modules ... VirtualBox Guest Additions: Building the VirtualBox Guest Additions kernel modules. VirtualBox Guest Additions: Running kernel modules will not be replaced until the system is restarted VirtualBox Guest Additions: Starting.`

![Modify message](image/webp;base64,UklGRuoAAABXRUJQVlA4TN0AAAAvE8AEEMegJpKt5v9PhRVaOvwrwEbOGXQwDACgTDZe6JP6/5DZ9pgGAJAG9we4gv8Lt5BcE9Mw/wEAWPeTFub0wPBT6JdDg9wYZ/+N/XLAA27k84hljs69ud9cs/z/Z5om9htPkgyM9ZZQDxUPMIwkScnz7i7kHyp/3FNEENF/RW7bNrbUfeozyN+t9YtK1bOCMVU/CDhJKeBgoPgy5S1jAV0mlhmFUgAIy5wFWpCCwfBQirx3r2vuPLIS5Stuh1TNnng/dmMEgRS/dlvrhbxh+BMEi/wpAvAE8AgqAQA= "Modify message")
