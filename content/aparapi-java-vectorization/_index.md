---
weight: 6
bookFlatSection: true
title: "Aparapi Java Vectorization"
---

# Aparapi Java Vectorization

Java is still at the early stages of supporting SIMD instructions. The only documentation claiming Java supports SIMD instructions is in bug reports, and in practice the Hotspot JIT  compiler never vectorized anything beyond a simple test program with a single sequential loop containing an array addition. Anytime threads were involved or the loop became more complicated the Hotspot JIT compiled to non SIMD instructions. Because of this, a special vector library is needed in order to enable SIMD operations in Java. Below you will find a link to a C++ vector library accessible to Java through JNI function calls as well as 10 Aparapi benchmarks comparing the performance of running Aparapi Java in the Java thread pool, with the vector library implemented, in a reduced looped kernel implementation, as well as on the GPU. README files with instructions on how to compile and run the benchmarks are included as well.

You can find more information about Aparapi Java Vectorization in the following paper and Virginia Tech thesis:
- Curt Albert, Alastair Murray and Binoy Ravindran, "[Applying Source Level Auto-Vectorization to Aparapi Java](/publications/pppj14.pdf)". International Conference on Principles and Practices of Programming on Java Platform: Virtual Machines, Programming Languages, and Tools (PPPJ '14), September 2014, Cracow, Poland
- Curt Albert, "[Applying Source Level Auto-Vectorization to Aparapi Java](https://vtechworks.lib.vt.edu/handle/10919/49022)", May 2014

Source code and documentation are available online on [sourceforge](http://sourceforge.net/projects/popcornlinux/files/aparapi_vectorization_tests.tar.xz/download).

**Contact**: Binoy Ravindran, Virginia Tech: binoy@vt.edu

---

This is an open-source project of the [Systems Software Research Group](https://www.ssrg.ece.vt.edu/) at [Virginia Tech](https://vt.edu/).

This work was supported in part by ONR under grant N00014-12-1-0880. Any opinions, findings, and conclusions or recommendations expressed in this site are those of the author(s) and do not necessarily reflect the views of ONR.