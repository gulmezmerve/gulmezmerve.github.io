---
title: 'crowdstrike'
date: 2024-07-20
permalink: /posts/2024/07/crowdstrike/
tags:
  - sdrad
  - cheri
---


The CrowdStrike outage shows that improving software resilience and availability is as important as detecting and mitigating memory-safety vulnerabilities.

I am exploring these aspects in my PhD research. 

As a solution, we propose "secure rewind and discard of isolated domains (SDRaD)" as an efficient and secure method of improving software resilience targeted by runtime attacks. [Rewind & Discard: Improving Software Resilience using Isolated Domains](https://lnkd.in/dZN7799Q). Even though my solution is for the user-space application, the same principle can be applied to kernel-space, too. 

We also work on improving software resilience for Rust applications when they are subject to unsafe code. [Friend or Foe Inside? Exploring In-Process Isolation to Maintain Memory Safety for Unsafe Rust](https://lnkd.in/dkkNi77t)

In a recent MSc thesis Sacha RUCHLEJMER, which I supervised, we explored improving the resiliency of CHERI in the Arm Morello prototype system with the principles developed for SDRaD. CHERI complements SDRaD well and allows many memory-safety problems to be detected before they corrupt memory, which makes recovering from CHERI-detected faults more efficient. [Secure Rewind and Discard on Arm Morello](https://lnkd.in/dVb5aSDW)

As a result, in the arms race between attacks and mitigations, we should also consider the effect on system availability and resiliency when memory-safety issues are detected!