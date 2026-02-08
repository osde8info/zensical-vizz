---
title: "oracle oci vms include 4 tuned profiles"
date: 2022-12-23
categories: 
  - "vizz"
---

oracle oci vms include 4 tuned profiles

```
# tuned-adm list
Available profiles:
- accelerator-performance     - Throughput performance based tuning with disabled higher latency STOP states
- balanced                    - General non-specialized tuned profile
- desktop                     - Optimize for the desktop use-case
- hpc-compute                 - Optimize for HPC compute workloads
- intel-sst                   - Configure for Intel Speed Select Base Frequency
- latency-performance         - Optimize for deterministic performance at the cost of increased power consumption
- network-latency             - Optimize for deterministic performance at the cost of increased power consumption, focused on low latency network performance
- network-throughput          - Optimize for streaming network throughput, generally only necessary on older CPUs or 40G+ networks
- oci-busy-polling            - Enable Busy Polling conditionally in OCI
- oci-cpu-power               - Set processor power management parameters in OCI
- oci-nic                     - Increase combined channels to 16 on NICs with bnxt_en driver on BM shapes in OCI
- oci-rps-xps                 - Enable RPS/XPS conditionally in OCI
- optimize-serial-console     - Optimize for serial console use.
- powersave                   - Optimize for low power consumption
- throughput-performance      - Broadly applicable tuning that provides excellent performance across a variety of common server workloads
- virtual-guest               - Optimize for running inside a virtual guest
- virtual-host                - Optimize for running KVM guests

Current active profile: oci-rps-xps oci-busy-polling oci-cpu-power oci-nic
```

see

https://www.redhat.com/en/blog/tuning-your-system-tuned
