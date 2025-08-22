---
weight: 10
bookFlatSection: true
title: "HeterSec - Software diversification using ISA heterogeneity"
---

# HeterSec - Software diversification using ISA heterogeneity

Software diversification is one of the most effective ways to defeat memory corruption-based exploits. Traditional software diversification mutates program memory layout and makes it difficult for attackers to pinpoint the precise location of a targeted vulnerability. Recent work illustrates the promise of improving software security using instruction-set-architecture (ISA) diversification.

<p align="center">
  <img src="/images/hetersec.png" alt="hetersec">
</p>

HeterSec is a software framework that enables application software diversification using ISA heterogeneity, utilizing off-the-shelf commodity machines of different ISAs (e.g., x86-64, AArch64). Leveraging the Popcorn Linux infrastructure, HeterSec hides the complex differences between ISAs including that between instructions, memory layout, registers, and ABIs, among others, and makes it easier to build and launch ISA-diversified application instances. To demonstrate HeterSec's objectives, the project has developed prototypes of two techniques that use ISA heterogeneity for software diversification as proofs-of-concept: multi-ISA-based moving target defense (MTD) and multi-ISA-based multi-version execution (MVX).

You can find more information about HeterSec in the following papers:

- [A Framework for Software Diversification with ISA Heterogeneity](https://www.ssrg.ece.vt.edu/papers/raid20.pdf), X. Wang, S. Yeoh, R. Lyerly, P. Olivier, S-H. Kim, and B. Ravindran, 23rd International Symposium on Research in Attacks, Intrusions and Defenses (RAID 2020), Donostia / San Sebastian, Spain, October 14-16, 2020
- [Secure and Efficient In-process Monitor (and Library) Protection with Intel MPK](https://www.ssrg.ece.vt.edu/papers/eurosec20.pdf), X. Wang, S. Yeoh, P. Olivier, and B. Ravindran, 13th European Workshop on Systems Security (EuroSec 2020), Co-located with EuroSys 2020, April 27, 2020, Heraklion, Crete, Greece


HeterSec's code is available on our [GitHub](https://github.com/ssrg-vt/HeterSec) as open-source software.

**Contact**:
- [Binoy Ravindran](https://ece.vt.edu/people/profile/ravindran), Virginia Tech,  binoy@vt.edu
- [Xiaoguang Wang](https://xiaoguang.wang/), Virginia Tech,  xiaoguang@vt.edu

---

HeterSec is an open-source project of the [Systems Software Research Group](https://ssrg.ece.vt.edu/) at [Virginia Tech](https://vt.edu/).

This work is supported in part by the US Office of Naval Research (ONR) under grants N00014-18-1-2022 and N00014-16-1-2711. Any opinions, findings, and conclusions or recommendations expressed in this site are those of the author(s) and do not necessarily reflect the views of ONR.
