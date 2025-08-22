---
weight: 9
bookFlatSection: true
title: "H-Container: Heterogeneous-ISA Container"
---

# H-Container

Edge computing is a recent computing paradigm that brings cloud services closer to the client. Among other features, edge computing offers extremely low client/server latencies. In order to consistently exploit the benefits of such low latencies, services need to run on edge nodes that are physically as close as possible to the clients. Thus, when a client changes physical location, a service should migrate between edge nodes to maintain proximity. Differently from data centers, edge nodes are often built with CPUs of different Instruction Set Architectures (ISA). Thus, a service that is natively compiled for one ISA cannot migrate to another, which hinders migration to the closest node.

H-Container enables the migration of containerized application, natively compiled, across compute nodes featuring CPUs of different ISAs. H-Container advances the state-of-the-art on heterogeneous-ISA migration systems on the following aspects:

- High compatibility. No source code or compiler toolchain modifications are needed.
- Easy deployability. H-Containers are fully implemented in user space, without any OS or hypervisor dependencies.
- Greater application support. Can migrate most Linux software, including server applications and dynamically linked binaries.

H-Container targets Linux, adopts LLVM, extends CRIU, and integrates with Docker. Experimental studies reveal that H-Container adds unnoticeable overheads during program execution and between 10ms and 100ms during execution migration. In real-world scenarios, H-Containers increases throughput – e.g., up to 94% increase in Redis throughput on heterogeneous-ISA platforms.

<p align="center">
  <img src="/images/hcontainer-concept.png" alt="hcontainer-concept">
</p>

You can find more information about H-Container in the following papers:
- [H-Container: Enabling Heterogeneous-ISA Container Migration in Edge Computing](https://dl.acm.org/doi/10.1145/3524452), T. Xing, A. Barbalace, P. Olivier, M. Karaoui, W. Wang, and B. Ravindran, ACM Transactions on Computer Systems, March 2022.
- Antonio Barbalace, Mohamed L. Karaoui,WeiWang, Tong Xing, Pierre Olivier, Binoy Ravindran, [Edge Computing – the Case for Heterogeneous-ISA Container Migration](/publications/hcontainer.pdf), In the  16th ACM SIGPLAN/SIGOPS International Conference on Virtual Execution Environments (VEE’20), March 17, 2020, Lausanne, Switzerland. Watch the video [here](https://www.youtube.com/watch?v=H0cKvYV9O4s).

Source code and documentation are available online on [GitHub](https://github.com/systems-nuts/hcontainer-tutorial/wiki):

- Popcorn Compiler “criu” branch https://github.com/systems-nuts/popcorn-compiler/tree/criu
	- How to start https://github.com/systems-nuts/popcorn-compiler/blob/master/README
- CRIU, two different branches based on the usage, for Docker “heterogeneous-simplified” is recommended
	- https://github.com/systems-nuts/criu-het/tree/crit-in-criu (default branch)
	- https://github.com/systems-nuts/criu-het/tree/heterogeneous-simplified
	- How to start https://github.com/systems-nuts/criu-het/wiki
- Docker tutorial and demo https://github.com/systems-nuts/hcontainer-tutorial     [YouTube Demo](https://www.youtube.com/watch?v=Gj9L169hg50&t=2s)

**Contact:**
- Binoy Ravindran, Virginia Tech: binoy@vt.edu
- Antonio Barbalace, University of Edinburgh: abarbala@ed.ac.uk

---

This is an open-source project of the [Systems Software Research Group](https://ssrg.ece.vt.edu/) at [Virginia Tech](https://vt/edu) and [System-nuts](http://github.com/systems-nuts) Group at [Stevens](http://www.stevens.edu/schaefer-school-engineering-science/departments/computer-science)/[The University of Edinburgh](http://www.ed.ac.uk/informatics).

This work was supported in part by US Office of Naval Research under grants N00014-16-1-2104, N00014-16-1-2711, and N00014-19-1-2493. Any opinions, findings, and conclusions or recommendations expressed in this site are those of the author(s) and do not necessarily reflect the views of AFOSR and ONR.