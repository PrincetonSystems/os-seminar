---
slug: l4
number: 6
title: "Term Project. Also the L4 Microkernel"
---

# Term Project

Three options:

  * Literature review of a particular topic.

  * Build a system or deeply evaluate an existing system.

  * Reproduce prior work

## General Criteria

  * Must grapple with at least one of the three trade-offs:

      1. Security vs Performance
      2. Security vs Extensibility
      3. Extensibility vs Performance

  * E.g.:

    * How does the system design or implementation trade performance for
      security?

    * How does a mechanism used in the system design or implementation trade
      help achieve better performance/security/extensibility without
      sacrificing performance/security/extensibility?

    * Where improvements in one or more of performance/security/extensibility
      "move?" E.g., sometimes throughput or latency improvements will "move" to
      increased code, memory, or power overheads.

    * What are empirical limitations of a systems abstraction that's considered
      "free"?

  * Think _small_

    * We're reading papers about systems that usually took many person-years to
      build. You don't have many person-years.
    * Often there is some central nugget that can be built much much faster.
    * Often it's multiple redesigns that takes so much effort. What can you do
      if you already know the answer? How much effort will the first
      (potentially wrong) iteration be?

  * Doesn't have to be a "system" as long as it's _related_ to systems. It could be:

    * Language runtime
    * Hardware
    * Library or framework

  * What is _related_ to systems? Must have some notion of different "programs" operating together or
      concurrently, that are somehow mutually-distrustful.

    * Networking systems deal with network traffic/flows from multiple endpoints.

    * Hardware can work _in service_ of an operting system's job (e.g., memory
      protection schemes, tagging, cache coloring, etc).

    * Libraries and frameworks are designed to help a variety of applications. Even one at a time might be considered "untrusted".
        * E.g., that `libsqlite` does give the user access to low-level
          database primitives might be important for ensuring the database
          isn't corrupted.


## Build or evaluate a system

If you build a reasonably substantial system, we will figure out a way to fit
it into the criteria above.

  * Some system XYZ but it supports third-party extensions (ActiveNetworks,
    extensible storage system, programmable cache)

  * Some _already programmable_ system, but it provides more flexibility to applications (e.g, Exokernel, SDN)

  * Improve security of a system while sacrificing minimal performance or extensibility

  * Evaluate the tradeoff in some existing system. e.g:

    * What security policies are expressible in FreeBSD's capsicum framework
      that are not expressible in UNIX permissions? What are the performance
      implications? Etc.

## Literature Review

A comprehensive review of the literature on some topic related to the tradeoff.

Previous examples included

  * Extensible distributed storage systems
  * Side-channel and covert channels
  * Emedded systems for non-digital computers

## Reproduce prior work

Redo some related work (e.g. one of the papers we've read) with a twist.

  * Spin used Modula-3 to isolate kernel extensions on the DEC Alpha
    workstation. Both Modula-3 and the Alpha are irrelevant today: reproduce
    Spin (or a subset prototype) using a modern language on modern hardware.

