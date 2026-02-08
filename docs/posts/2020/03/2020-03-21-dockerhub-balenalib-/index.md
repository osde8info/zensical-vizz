---
title: "dockerhub balenalib iot base images"
date: 2020-03-21
categories: 
  - "vizz"
---

dockerhub has over 2000 balenalib iot base images

- https://hub.docker.com/u/balenalib/
- https://www.balena.io/docs/reference/base-images/base-images

balena have recently switched away from resin

https://www.balena.io/docs/reference/base-images/base-images/#major-changes

- _`UDEV` now defaults to `off`, so if you have code that relies on detecting dynamically plugged devices, you will need to enable this in either your Dockerfile or via a device environment variable. See [Working with Dynamically Plugged Devices](https://www.balena.io/docs/reference/base-images/base-images/#working-with-dynamically-plugged-devices)._
- _The `INITSYSTEM` functionality has been completely removed, so applications that rely on [systemd](https://www.freedesktop.org/wiki/Software/systemd/) or [openRC](https://github.com/OpenRC/openrc) should install and set up the initsystem in their apps. See [Installing your own Initsystem](https://www.balena.io/docs/reference/base-images/base-images/#installing-your-own-initsystem)._
- _Mounting of `/dev` to a devtmpfs will now only occur when `UDEV=on` and the container is running as `privileged`. `1`, `true` and `on` are valid value for `UDEV` and will be evaluated as `UDEV=on`, all other values will turn `UDEV` off._
- _Support for Debian Wheezy has been dropped._
- _`armel` architecture has been renamed to `armv5e`._
