---
weight: 7
bookFlatSection: true
title: "AIRA CPU/GPU Resource Management"
---

# Automatic Instrumentation for Resource Adjustment (AIRA)

<br />

<p align="center">
  <img src="/images/software_stack.png" alt="software_stack">
</p>

In recent years, diminishing returns in single-core processor performance due to the end of the “free lunch” has pushed hardware design towards increasing levels of parallelism and heterogeneity. Whether it be out-of-order latency-oriented multicore CPUs or massively parallel throughput-oriented GPGPUs, modern hardware is becoming increasingly diverse in order to continue performance scaling for a wide range of applications. It is clear that platforms will become increasingly heterogeneous, meaning that developers must embrace this new hardware diversity to achieve higher performance.

Programming frameworks such as OpenMP and OpenCL have emerged as industry standards for programming parallel and heterogeneous platforms. These frameworks are functionally portable in that they allow developers to parallelize applications to target different types of processors. In particular, they specify a write-once, run-anywhere interface that allows developers to write a single compute kernel (a computationally-intense portion of an application) that is runnable on many different architectures. However, the developer is responsible for orchestrating application execution on processors in the platform, a cumbersome and error-prone process. The developer must select an architecture by extensively profiling the compute kernel on all available processors (assuming exclusive access to the system), manually direct data transfers between disjoint memory spaces and initiate compute kernel execution on the pre-selected processors. More importantly, these programming frameworks provide no mechanisms for flexible execution of compute kernels in platforms with dynamic and variable workloads because they require developers to hard-code processor selections at compile-time. Static decisions limit compute kernel execution efficiency and platform utilization in the face of diverse platform workloads. Dynamically selecting a set of processing resources on which to execute computation will become increasingly important as heterogeneous systems become ubiquitous in platforms with varying workloads.

AIRA (Application Instrumentation for Resource Adjustment) is a compiler and run-time system for automatically instrumenting and analyzing applications for flexible execution in heterogeneous platforms. AIRA is composed of several software components which automate selecting and sharing architectures at runtime, including a compute kernel analysis tool, a source-to-source compiler and a pluggable daemon for dynamic mapping of computation onto processor resources. AIRA targets co-executing OpenMP applications in dynamic workload settings.

You can find more information about AIRA in the following paper and Virginia Tech thesis:
- [AIRA: A Framework for Flexible Compute Kernel Execution in Heterogeneous Platforms](http://ieeexplore.ieee.org/document/8063925/), Robert Lyerly, Alastair Murray, Antonio Barbalace, Binoy Ravindran, IEEE Transactions on Parallel and Distributed Systems (TPDS), 2017
- Rob Lyerly, "[Automatic Scheduling of Compute Kernels Across Heterogeneous Architectures](https://vtechworks.lib.vt.edu/handle/10919/78130)", May 2014

Source code and documentation are available online on [GitHub](https://github.com/ssrg-vt/aira).

**Contact**: Binoy Ravindran, Virginia Tech: binoy@vt.edu

---

This is an open-source project of the [Systems Software Research Group](https://ssrg.ece.vt.edu/) at [Virginia Tech](https://vt.edu/).

This work was supported in part by ONR under grant N00014-12-1-0880. Any opinions, findings, and conclusions or recommendations expressed in this site are those of the author(s) and do not necessarily reflect the views of ONR.