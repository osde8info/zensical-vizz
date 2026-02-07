---
title: "Installing MS Azure CLI in WSL Ubuntu"
date: 2020-03-11
categories: 
  - "vizz"
tags: 
  - "cli"
  - "install"
  - "ms-azure"
---

Installing MS Azure CLI in WSL Ubuntu

read

- https://docs.microsoft.com/en-gb/cli/azure/install-azure-cli-linux?view=azure-cli-latest

but run

```
# aptitude install build-essential libssl-dev libffi-dev python3-dev
# curl -L https://aka.ms/InstallAzureCli | bash
```

as root and change install path from ~/ to

- /opt/azcli

and logout as root and add this to the end of YOUR  .bashrc

```
export PATH=$PATH:/opt/azcli

source '/opt/azcli/az.completion'
```
