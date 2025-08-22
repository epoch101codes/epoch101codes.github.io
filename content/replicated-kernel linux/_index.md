---
weight: 3
bookFlatSection: true
title: "Replicated-kernel Linux"
---

# Replicated-kernel Linux
Performance scalability of software running on highly parallel, general-purpose (homogeneous) CPUs has been shown to be a problem. In fact, performance of software written for shared memory multiprocessors or multicores may suffer when multiple CPUs synchronize on the same variable or access the same variable in parallel – this is because, cache coherency, which provides shared memory, has a non-negligible cost when the number of CPUs is high. Additionally, the CPU topology may contribute to an increase in memory access latency. 

The very first version of Popcorn Linux addressed this problem at the operating system level. Popcorn Linux recognizes that application software scalability may be hindered by operating system scalability and redesigns the Linux operating system kernel as a multiple kernel OS. In this design, each CPU, or group of CPUs (e.g., a NUMA node) runs a different Linux kernel instance. Instances do not share memory, and communicate via message passing (similar to a [multikernel OS](http://www.barrelfish.org/)). Each operating system service is rewritten as a distributed service (the project focused only on a subset of Linux services). We call this model "replicated-kernel OS". Popcorn Linux's replicated-kernel model demonstrated that the multiple kernel OS design based on a “shared nothing” model (cf. multikernel) can also be successfully applied to monolithic kernels and achieve similar speedups.

<p align="center">
  <img src="/images/replicated-kernel.png" alt="replicated-kernel">
</p>

You can find more information about Popcorn as a replicated-kernel Linux in the following papers and Virginia Tech thesis:
- Marina Sadini, Antonio Barbalace, Binoy Ravindran and Francesco Quaglia, ["A Page Coherency Protocol for Popcorn Replicated-kernel Operating System"](http://popcornlinux.org/images/publications/marc2013_camera_ready_fixed.pdf). 2013 Many-Core Architecture Research Community (MARC '13) Symposium. Co-located with ACM SIGPLAN conference on Systems, Programming, Languages and Applications: Software for Humanity (SPLASH), October 2013, Indianapolis, Indiana, USA
- Antonio Barbalace, Binoy Ravindran and David Katz, ["Popcorn: a replicated-kernel OS based on Linux"](http://popcornlinux.org/images/publications/barbalace_ols.pdf). The 2014 Ottawa Linux Symposium (OLS '14), July 2014, Ottawa, Canada [[dreamhosters link]](http://nw.dreamhosters.com/ols/ols2014/)
- David Katz, Antonio Barbalace, Saif B.M. Ansary, Akashay Ravichandran and Binoy Ravindran, ["Thread Migration in a Replicated-kernel OS"](http://popcornlinux.org/images/publications/icdcs2015_david.pdf). The 35th International Conference on Distributed Computing Systems (ICDCS XXXV), June 2015, Columbus, Ohio, USA
- David Katz, ["Popcorn Linux: Cross Kernel Process and Thread Migration in a Linux-Based Multikernel"](https://vtechworks.lib.vt.edu/handle/10919/52561), MS Thesis, Virginia Tech, September 2014

Source code and documentation is available online on [sourceforge](https://sourceforge.net/p/popcornlinux/code/ci/master/tree/).

**Contact**: Binoy Ravindran, Virginia Tech:  [binoy@vt.edu](mailto:binoy@vt.edu)

---

This is an open-source project of the [Systems Software Research Group](https://www.ssrg.ece.vt.edu/) at [Virginia Tech](https://vt.edu/).

This work was supported in part by ONR under grants N00014- 12-1-0880 and N00014-13-1-0317, and by US NSWC under contract N00178-09-D-3017/0022.  Any opinions, findings, and conclusions or recommendations expressed in this site are those of the author(s) and do not necessarily reflect the views of ONR and NSWC. 