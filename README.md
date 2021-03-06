# Bao - a lightweight static partitioning hypervisor

Introduction
------------

test

**Bao** (from Mandarin Chinese “bǎohù”, meaning “to protect”) is a lightweight, 
open-source embedded hypervisor which aims at providing strong isolation and 
real-time guarantees. Bao provides a minimal, from-scratch implementation of 
the partitioning hypervisor architecture. 

Designed mainly for targeting mixed-criticality systems, Bao strongly focuses 
on isolation for fault-containment and real-time behavior. Its implementation 
comprises only a minimal, thin-layer of privileged software leveraging ISA 
virtualization support to implement the static partitioning hypervisor architecture: 
resources are statically partitioned and assigned at VM instantiation time; 
memory is statically assigned using 2-stage translation; IO is pass-through only; 
virtual interrupts are directly mapped to physical ones; and it implements a 1-1 
mapping of virtual to physical CPUs, with no need for a scheduler. 

Bao has no external dependencies, such as on privileged VMs running untrustable, 
large monolithic general-purpose operating systems (e.g., Linux), and, as such, 
encompasses a much smaller TCB..

Bao originally targets the Armv8-A architecture, but there is already support
for the RISC-V architecture. The full list of supported (and work in progress) 
platforms is presented below:

- [x] Xilinx Zynq UltraScale+ MPSoC ZCU102 (Armv8-A)
- [x] Xilinx Zynq UltraScale+ MPSoC ZCU104 (Armv8-A)
- [x] Ultra96 Zynq UltraScale+ ZU3EG (Armv8-A)
- [x] NXP MCIMX8QM-CPU (Armv8-A)
- [x] NVIDIA Jetson TX2 (Armv8-A)
- [x] 96Boards HiKey 960 (Armv8-A)
- [x] Raspberry Pi 4 (Armv8-A)
- [x] QEMU virt (Armv8-A)
- [x] QEMU virt (RISC-V rv64)
- [ ] Rocket w/ H-extension (RISC-V rv64) - soon
- [ ] NXP MCIMX8M-EVK (Armv8-A) - soon
- [ ] 96Boards ROCK960 (Armv8-A) - wip




**NOTE**: This is work in progress! Don't expect things to be complete. 
Use at your own risk.



Community Resources
-------------------

Project website:

 - http://www.bao-project.org/ 

Source code:

 - https://github.com/bao-project/bao-hypervisor.git
 - git@github.com:bao-project/bao-hypervisor.git

 Contributing:
 
 - Please get in touch (info@bao-project.org)



Demos
------------

A tutorial providing a step-by-step guide on how to run different demo
configurations of the Bao hypervisor featuring multiple guest operating
systems and targeting several supported platforms will be released soon!



References
------------

4. Bruno Sá, José Martins and Sandro Pinto. "**A First Look at RISC-V Virtualization from an Embedded Systems Perspective**".
To be published, 2021.
https://arxiv.org/abs/2103.14951


3. José Martins and Sandro Pinto. "**Static Partitioning Virtualization on RISC-V**".
In RISC-V Summit, virtual, 2020. 


2. José Martins and Sandro Pinto. "**Bao: a modern lightweight embedded hypervisor**".
In Proceedings of the Embedded World Conference, Nuremberg, Germany, 2020. 


1. José Martins, Adriano Tavares, Marco Solieri, Marko Bertogna, and Sandro Pinto. 
"**Bao: A Lightweight Static Partitioning Hypervisor for Modern Multi-Core Embedded 
Systems**". In Workshop on Next Generation Real-Time Embedded Systems (NG-RES 2020). 
Schloss Dagstuhl-Leibniz-Zentrum für Informatik. 2020.
https://drops.dagstuhl.de/opus/volltexte/2020/11779/
