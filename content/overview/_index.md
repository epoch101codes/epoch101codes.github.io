---
weight: 2
bookFlatSection: true
title: "Overview"
---

# Overview
The project has developed the first version of a replicated kernel OS model for Linux, called Popcorn Linux. This version implements a set of techniques to support replicated-kernel execution and ISA heterogeneity, including that for the boot process, processor grouping, memory management, device driver management, and inter-kernel communication. Popcorn currently runs on x86 64bit architectures. (We also have an unmaintained port on x86 32bit.)

## Booting
To boot Linux on a subset of hardware resources we added Linux boot parameters to limit the hardware resource discovered, initialized and loaded by any kernel. After the first kernel is loaded by the bootloader, other, secondary, kernels can be loaded from this primary kernel by a modified version of _**kexec**_. We developed a new version of the Linux _**trampoline**_ code to boot a secondary kernel on x86.


## Communicating Kernels
Kernels communicate by messages. Each time a kernel boots up, it registers itself on the messaging layer. We define a set of services that can register notifications on every kernel, but only the interested kernels are notified. The current implementation uses a combination of messages over shared memory and inter-processor interrupts with an interrupt mitigation strategy similar to the NAPI layer.

## Interacting with different Kernels
We implemented a high-performance in-kernel virtual network interface, that allows processes running on secondary kernels to have network access if required.  Applications, however, can rely on standard inter-process communication techniques, like shared memory, which works on multiple kernels operating on cache coherent kernels ,or message-passing on other hardware.  For example, we used inter-kernel shared memory to provide a MPICH2 Nemesis channel for running MPI applications on Popcorn.  Finally, if the user needs to log into a secondary kernel directly, for debugging purposes, then they can ssh over the in-kernel virtual network, or we provide virtual TTYs between kernels for when the networking itself needs debugging.

## Usage Scenarios

Popcorn Linux can be used as:

- A single system image operating system for future heterogeneous-ISA platforms.
- An alternative to virtualization, although not as secure as virtual machines, Popcorn extensions to the Linux kernel enable kernel instances to run on the same physical machine without paying the overhead of virtualization.
- A compute node/IO node configuration (also called full and light kernels); you can compile two different kernel images, one with all device drivers and services and the other with a minimal processor support along with a minimal ramdisk.
- To run an application in isolation; a real-time kernel can run its application in total isolation while all other kernels can provide services while not interfering with the real-time execution.
- A monolithic replicated-kernel operating system for educational and research purposes.
