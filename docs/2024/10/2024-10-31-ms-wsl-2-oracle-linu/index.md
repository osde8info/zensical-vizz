---
title: "ms wsl 2 oracle linux 8/9 firefox GUI errors"
date: 2024-10-31
categories: 
  - "vizz"
tags: 
  - "gfx"
  - "gui"
  - "linux"
  - "oracle-linux"
  - "programming"
  - "security"
  - "wsl"
---

win 10 oracle linux 8

```
$ firefoxSafe Browsing server returned a 400 during update:requesturl = https://safebrowsing.googleapis.com/v4/threatListUpdates:fetch?$ct=application/x-protobuf&key=please-replace-me&$httpMethod=POST, payload =Crash Annotation GraphicsCriticalError: |[0][GFX1-]: RenderCompositorSWGL failed mapping default framebuffer, no dt (t=8.4834)[GFX1-]: RenderCompositorSWGL failed mapping default framebuffer, no dt$ Crash Annotation GraphicsCriticalError: |[0][GFX1-]: RenderCompositorSWGL failed mapping default framebuffer, no dt (t=3.80344)[GFX1-]: RenderCompositorSWGL failed mapping default framebuffer, no dtSafe Browsing server returned a 400 during update:requesturl = https://safebrowsing.googleapis.com/v4/threatListUpdates:fetch?$ct=application/x-protobuf&key=please-replace-me&$httpMethod=POST, payload = C$ Safe Browsing server returned a 400 during update:request url = https://safebrowsing.googleapis.com/v4/threatListUpdates:fetch?$ct=application/x-protobuf&key=please-replace-me&$httpMethod=POST, payload =
```

win 11 oracle linux 9

```
$ firefoxCrash Annotation GraphicsCriticalError: |[0][GFX1-]: glxtest: libEGL initialize failed (t=1.41012)[GFX1-]: glxtest: libEGL initialize failedCrash Annotation GraphicsCriticalError: |[0][GFX1-]: glxtest: libEGL initialize failed (t=1.41012) |[1][GFX1-]: glxtest: EGL test failed (t=1.41012)[GFX1-]: glxtest: EGL test failedSafe Browsing server returned a 400 during update:requesturl = https://safebrowsing.googleapis.com/v4/threatListUpdates:fetch?$ct=application/x-protobuf&key=please-replace-me&$httpMethod=POST, payload =Crash Annotation GraphicsCriticalError: |[0][GFX1-]: glxtest: libEGL initialize failed (t=1.41012) |[1][GFX1-]: glxtest: EGL test failed (t=1.41012) |[2][GFX1-]: RenderCompositorSWGL failed mapping default framebuffer, no dt (t=346.87)[GFX1-]: RenderCompositorSWGL failed mapping default framebuffer, no dt
```
