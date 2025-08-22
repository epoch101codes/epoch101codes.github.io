---
weight: 5
bookFlatSection: true
title: "Fault-Tolerant Linux"
---

# Fault Tolerant Linux

FT-Linux pioneers full-software stack fault-tolerance on a single SMP machine based on the Linux software ecosystem, demonstrating -- through a proof-of-concept -- that  monolithic operating systems such as Linux can be made fault resilient.

FT-Linux enables Linux to tolerate transient and permanent hardware failures. FT-Linux is built on top of the replicated-kernel version of Linux, Popcorn Linux, and aims to provide fault tolerance along the whole software stack, from the OS kernel to  applications. FT-Linux targets SMP machines in which there are multiple core/processor domains as well as memory controllers (and eventually I/O controllers), with the presumption that each of them may fail independently. Two main categories of faults are considered: a) permanent failures such as fail-stop errors and b) transient errors such as bit-flops in main memory.

<p align="center">
  <img src="/images/ftlinux.png" alt="ftlinux">
</p>
 

You can find more information about FT-Linux in the following papers and Virginia Tech thesis: 
- Giuliano Losa, Antonio Barbalace, Yuzhong Wen, Marina Sadini, Ho-Ren Chuang, and Binoy Ravindran, "[Transparent Fault-Tolerance using Intra-Machine Full Software Stack Replication](/publications/ftos_icdcs17.pdf)", The 37th IEEE International Conference on Distributed Computing Systems (ICDCS 2017), June 5-8, 2017, Atlanta, Georgia, USA 
- Giuliano Losa, Antonio Barbalace, Yuzhong Wen, Marina Sadini and Binoy Ravindran, "[Transparent Intra-machine Full-Software-Stack Replication for Fault Tolerance](/publications/CloudDP_2016.pdf)". Short Paper. The 6th Workshop on Cloud Data and Platforms (CloudDP '16). Co-located with the 2016 ACM European Conference on Computer Systems (EuroSys 2016), April 2016, London, United Kingdom
- Yuzhong Wen, "[Replication of Concurrent Applications in a Shared Memory Multikernel](https://vtechworks.lib.vt.edu/handle/10919/71813)", June 2016

Source code and documentation is available online on GitHub. 
 
**Contact**: Binoy Ravindran, Virginia Tech:  binoy@vt.edu

---

This is an open-source project of the [Systems Software Research Group](https://www.ssrg.ece.vt.edu/) at [Virginia Tech](https://vt.edu/).

This work is supported in part by AFOSR (grants FA9550-14-1-0163 and FA9550-16-1-0371) and ONR (grants N00014-13-1-0317 and N00014-16-1-2711). Any opinions, findings, and conclusions or recommendations expressed in this site are those of the author(s) and do not necessarily reflect the views of AFOSR and ONR. 