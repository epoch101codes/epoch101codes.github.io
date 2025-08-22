---
weight: 4
bookFlatSection: true
title: "NetPopcorn"
---

# NetPopcorn

Some OS subsystems may suffer performance scalability more than others. This is the case, for example, with the Linux network stack. With increasingly fast network cards, any network stack cross-CPU synchronization may hinder packet processing latency – fundamental in the data-center (cf. tail latency) or in telecommunication and network appliances. NetPopcorn extends the replicated-kernel OS model of Popcorn Linux with a distributed network stack implementation and a distributed device driver model (Snap Bean). NetPopcorn shows better performance than Linux and state-of-the-art research efforts on Linux, as well as nearing the same performance as kernel-bypass solutions (cf. DPDK).

<p align="center">
  <img src="/images/netpopcorn.png" alt="netpopcorn">
</p>

 You can find more information about NetPopcorn in the following paper and Virginia Tech thesis:
- [A Distributed Operating System Network Stack and Device Driver for Multicores](/publications/netpopcorn_icdcs17.pdf), B. M. Saif Ansary, Antonio Barbalace, Binoy Ravindran, Thomas Lazor, and Ho-Ren Chuang, The 37th IEEE International Conference on Distributed Computing Systems (ICDCS 2017), Short paper, June 5-8, 2017, Atlanta, Georgia, USA 
- B.M. Saif Ansary, "[High Performance Inter-kernel Communication and Networking in a Replicated-kernel Operating System](https://vtechworks.lib.vt.edu/handle/10919/78338)", September 2015

Source code and documentation is available online on [sourceforge](https://sourceforge.net/p/popcornlinux/code/ci/netpopcorn/tree/). 
 
**Contact**: Binoy Ravindran, Virginia Tech: binoy@vt.edu
---
This is an open-source project of the [Systems Software Research Group](https://ssrg.ece.vt.edu/) at [Virginia Tech](https://vt.edu/).

This work was supported in part by ONR under grants N00014- 13-1-0317 and N00014-16-1-2711, AFOSR under grant FA9550- 14-1-0163, and NAVSEA/NEEC under grants 3003279297 and N00174-16-C-0018. Any opinions, findings, and conclusions or recommendations expressed in this site are those of the author(s) and do not necessarily reflect the views of ONR, AFOSR, and NAVSEA/NEEC.