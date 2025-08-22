---
weight: 8
bookFlatSection: true
title: "HEXO - Heterogeneous-ISA EXecution Offloading of Unikernel VMs"
---

# HEXO - Heterogeneous-ISA EXecution Offloading of Unikernel VMs

Today, OS-capable embedded systems exhibiting a very low power consumption are available at an extremely low price point. These characteristics make them highly compelling in a datacenter context. Our approach, named Heterogeneous EXecution Offloading (HEXO), selectively offloads Virtual Machines (VMs) from fast server class machines to slow embedded boards. HEXO shares long-running, compute intensive datacenter workloads between a server machine and one or a few connected embedded boards of negligible cost and power consumption, bringing significant benefits in terms of consolidation. 

Designed with performance in mind, HEXO runs native code. We address the Instruction Set Architecture (ISA) difference between typical servers (e.g., x86) and embedded systems (e.g., ARM) through hypervisor and guest OS-level support for heterogeneous-ISA runtime VM migration, leveraging the Popcorn Linux compiler. We cope with the low amount of resources in embedded systems by using lightweight VMs: unikernels. VMs are offloaded based on an estimation of the slowdown expected from running on a given embedded board.

<p align="center">
  <img src="/images/hexo-overview.png" alt="hexo-overview">
</p>

You can find more information about HEXO in our [HPDC'19 paper](https://www.ssrg.ece.vt.edu/papers/hpdc19.pdf) and [poster](/publications/hexo-poster.pdf), as well as in A K M Fazla Mehrab's [thesis](https://vtechworks.lib.vt.edu/handle/10919/86485). HEXO's source code and documentation is available online on [GitHub](https://github.com/ssrg-vt/popcorn-compiler/tree/hermit-master).

**Contact**: [Pierre Olivier](https://sites.google.com/view/pierreolivier), Virginia Tech: polivier <at> vt <dot> edu

---

HEXO is an open-source project of the [Systems Software Research Group](https://ssrg.ece.vt.edu/) at [Virginia Tech](https://vt.edu).

HEXO is supported by ONR under grants N00014-16-1-2104 and N00014-16-1-2711. Any opinions, findings, and conclusions or recommendations expressed in this site are those of the author(s) and do not necessarily reflect the views of ONR. 

This research and development is also supported by the German Federal Ministry of Education and Research under Grant 01IH16010C (Project ENVELOPE).