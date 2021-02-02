---
slug: microkernels
number: 4
title: Isolation, flexibility, but not performance!
---

Microkernels
============

  * Definition: Kernel implements address spaces, IPC, "basic" scheduling

  * Presumed benefits:

    * Coexisting APIs (Windows vs. Linux API just two different servers)

    * More easily portable: only selected servers need modification to port to
      new hardware or support new applications.

    * "Egalitarian" - all servers can use kernel mechanisms

    * Safety -- server malfunctions are isolated

      * Including device drivers?

    * Less error prone

    * Smaller TCB: hardware, microkernel, disk driver, file system

  * Key enablers:

    * External pager

    * "everything is an IPC"

      - Can drivers actually be added dynamically? What about device state? What about driver state that applications rely on?

      - How do loadable kernel modules differ in terms of extensibility?

  * First example of a benchmark for how much performance is enough:

    - Existing applications should not experience degraded performance

    - New applications must be enabled that cannot be implemented efficiently

  * Key weaknesses in first generation:

    * RPC overhead vs. time spent in user space between RPCs

    * User-level pagers not really good enough. Need control of virtual memory

    * Why? Posits that it's because most microkernels evolved from monolothic kernels. Not a real microkernel.

  * Second generation:

    * RPC overhead not fundamental

    * Insight, microkernel needs to be hardware dependent

      * Not just a matter of recompiling for a different architecture, but different data structures and algorithms

    * L4: mechanism vs policy
