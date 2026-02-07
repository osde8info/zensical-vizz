---
title: "Add a sound card and USB to a VMware Player VM"
date: 2007-04-02
categories: 
  - "vizz"
---

Edit the VMX file and ADD sound

sound.present = "TRUE" sound.fileName = "-1" sound.autodetect = "TRUE" ADD USB

usb.present = "TRUE" usb.generic.autoconnect = "FALSE"
