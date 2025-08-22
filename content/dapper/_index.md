---
weight: 11
bookFlatSection: true
title: "Dapper - Cross-ISA Process Snapshot Rewriting"
---

# Dapper - Cross-ISA Process Snapshot Rewriting

Dapper transforms a live process's state for different purposes. For example, Dapper supports live process migration of natively compiled Linux binaries across servers with CPUs of different architectures. It also supports re-randomizing the stack and registers of a process to improve security.

<p align="center">
  <img src="/images/dapper-overview.png" alt="dapper-overview">
</p>

Dapper was built on top of [CRIU](https://criu.org/Main_Page) to dump a running process and then transform the [CRIU images](https://criu.org/Images) to support restoration on servers of a different architecture. Currently, Dapper supports process migration on x86-64 and aarch64 CPUs.You can find more information about Dapper in the following paper:
- Dapper: A Lightweight and Extensible Framework for Live Program State Rewriting. A. Bapat, J. Shastri, X. Wang, A. Sundarasamy, and B. Ravindran to appear in IEEE ICDCS'24 [[Paper](https://ssrg.ece.vt.edu/papers/icdcs24.pdf)] [[Code](https://github.com/dapper-project/dapper)]

Dapper's code is available on our [GitHub](https://github.com/dapper-project/dapper) as open-source software. You can also find a [Demo](https://github.com/dapper-project/demo) of how Dapper works.

**Contact**:
- [Binoy Ravindran](https://ece.vt.edu/people/profile/ravindran), Virginia Tech,  binoy@vt.edu
- [Xiaoguang Wang](https://xiaoguang.wang/), University of Illinois Chicago, xgwang9@uic.edu

---

Dapper is an open-source project of the [Systems Software Research Group](https://ssrg.ece.vt.edu/) at [Virginia Tech](https://vt.edu/) and the [University of Illinois Chicago](https://uic.edu/).

This work is supported in part by the US Office of Naval Research (ONR) under grants N00014-18-1-2022, N00014-19-1-2493, and N0001422-1-2672 and by the US National Science Foundation (NSF) under grant CNS 2127491. Any opinions, findings, conclusions, or recommendations expressed in this site are those of the author(s) and do not necessarily reflect the views of ONR or NSF.