---
title: "Windows WSL &amp; Cockpit &amp; Podman"
date: 2022-12-19
categories: 
  - "vizz"
---

Windows WSL & Oracle 8 & Cockpit & Podman

- https://cockpit-project.org/running.html#rhel

- https://podman.io/getting-started/installation#windows

- https://github.com/containers/podman/blob/main/docs/tutorials/podman-for-windows.md

- https://github.com/containers/podman/releases

```
[cdarra@DESKTOP-EJTS2G0 ~]$ podman images
REPOSITORY                 TAG         IMAGE ID      CREATED      SIZE
docker.io/library/python   latest      539eccd5ee4e  12 days ago  954 MB
docker.io/library/busybox  latest      334e4a014c81  13 days ago  5.09 MB
docker.io/library/alpine   latest      49176f190c7e  3 weeks ago  7.34 MB
[cdarra@DESKTOP-EJTS2G0 ~]$ podman ps
CONTAINER ID  IMAGE                             COMMAND     CREATED         STATUS             PORTS       NAMES
0f7c2bc0aab5  docker.io/library/busybox:latest  sh          6 minutes ago   Up 6 minutes ago               quizzical_gauss
98ccc3e4ead6  docker.io/library/alpine:latest   sh          21 seconds ago  Up 21 seconds ago              kind_hofstadter
90c90a9b41f6  docker.io/library/python:latest   sh          21 seconds ago  Up 20 seconds ago              gifted_cori
```

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/wslfire-1.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/wslfire-1.png)

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/wslubufire-1.png?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/wslubufire-1.png)

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/web-capture_19-12-2022_18181_172.22.149.241-1.jpeg?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/web-capture_19-12-2022_18181_172.22.149.241-1.jpeg)

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/web-capture_19-12-2022_182639_172.22.149.241-1.jpeg?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/web-capture_19-12-2022_182639_172.22.149.241-1.jpeg)

[![](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/web-capture_20-12-2022_10477_localhost-1.jpeg?w=1024)](https://vizz8info.wordpress.com/wp-content/uploads/2022/12/web-capture_20-12-2022_10477_localhost-1.jpeg)
