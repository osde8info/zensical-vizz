---
title: "vercel cli build python apps"
date: 2026-01-25
categories: 
  - "vizz"
---

to get the vercel cli to build python (mkdocs) apps locally you need to install uv

first update your .gitignore

```
.vercel
.vercel_python*

```

then

```
dnf install pipx
dnf install python3-mkdocs
dnf install mkdocs-material

pipx install uv

vercel build
vercel dev
```
