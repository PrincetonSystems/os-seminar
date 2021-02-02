---
slug: welcome
number: 1
title: "What is an Operating System?"
---

# Introductions

## Students

  * Name

  * Masters? PhD? Year?

  * Areas of interest?

  * What projects are you working on?

  * Recent work you enjoyed

## Me first

  * Who am I?

    * Amit Levy

    * New Assistant Professor

    * "Secure": OS, distributed systems, storage systems, web platforms... really systems in general

      - Building systems that are as flexible as _reasonable_ for application developers

    * Most active current work is a secure operating system for low-memory microcontrollers

      * Also looking at co-designing hardware/language/OS, general kernel
        security, distributed cache characterization with Wyatt, runtimes for
        FaaS, IoT network protocols. If someone wants to talk about the kitchen as an OS, please talk to me
        too.

    * Recent work I loved: Salsify by Sadjad Fouladi (NSDI 2018)

# What will today's class look like?

  * Not going over the syllabus today, but high-level: paper-reading class, with a course project.

  * Goal today is to give a flavor at the scope of what we'll cover and _how_
    we're going to look at operating systems during the semester.

  * Some ground rules:

    * Be excellent to each other

    * We're operating in a broad field at a very high level.

    * I expect you to wear your knowledge and understanding gaps on your
      sleeves, and I also expect you to create a positive environment for that.

    * Assume good intentions

  * Two modes when reviewing paper/proposals/ideas:

    1. What can I learn from this work? What is interesting? What is cool?

    2. What problems does this work have? Where are there mistakes? What should
       I be skeptical about? How could it improve?

# What is an "Operating System"?

## On the board

  * What are examples of operating systems?

    * Want to hit: kernels, "Desktop Environments," Distributed Systems, Databases, Web Platforms

    * Linux, Windows, Darwin, FreeBSD, etc...

      * Commonly called "kernels"

    * Android, iOS, GNOME Desktop, etc...
 
      * Kernel + drivers for particular hardware + software services + userland APIs

    * Hypervisors: Xen et al

    * Databases:

      * SQL queries are the applications

      * Sometimes users are even _explicit_

      * Hardware resources: the data, software resources: indexes, stored procedures, etc?

    * Distributed systems?

      * DHTs?

      * Paxos?

      * Bitcoin? Ethereum?

    * Web platforms: Facebook API? Rails?

## In groups (3-5 groups)

  * Take one of the categories and find an example that _is_ an operating system and one that _isn't_.

  * Each group presents their examples and we discuss

## On the board

  * What makes something an OS?

    * Applications?

    * Users?

    * Resources?

  * Why might something _not_ be an OS?

    * Single-application/single-user? Is a web framework an OS? What about embedded systems? Click?

    * Does it need a computer?

      * Amazon Turk?

    * Does it have to be software?

  * My definition: Software that manages a computer's resources for its users and their applications.

    * Generally try to provide: extensible, safe, and performant access to hardware and software services.

    * Triangle of trade-offs

# Extensibility, Safety, Performance

## On the board

  * What is extensibility? What is the most exterme form of extensibility?

    * Every app can do literally whatever it wants (e.g. everything in ring-0)

    * Examples? (Linux drivers)

  * What is safety? What is the most extreme form of safety?

    * Every app can do exactly nothing---no way for apps to interfere with each other doing nothing.

    * Examples? (key-value store get/set requests, sort of)

  * What is performance? What is the most extreme form of performance?

    * Only one application that has complete access

# Isolation Mechanisms

How a system navigates this trade-off comes down to:

  * Choice of isolation mechanism

  * Abstractions and interfaces using that isolation mechanism

    * E.g. light-weight contexts doesn't change the isolation mechanism, but designs a new interface for it.

Three broad categories of isolation mechanisms:

  * Hardware-based isolation

    * Advantage: high performance for CPU-bound workloads (address-translation is fast)

    * Disadvantages:

      1. Communication between processes/kernel is expensive

      2. Usually fixed number of protection levels

      3. Typically couples execution thread with access control

  * Software-based fault isolation (SFI)

    * Examples: early VMWare (before x86 had virtualization hardware), NaCL in Chrome (before WebAssembly)

    * Advantages: Lighter-weight communication than hardware

    * Disadvantage: common-case performance is worse. Anecdotally also hard to get right.

  * Type-safe languages

    * Examples: JavaScript in the browser, PHP on web servers

    * Advantages:

      - Very flexible

      - Non-heirarchical

      - More expressive (can articulate finer-grained protection than a memory address)

      - Easier to change and extend compilers than hardware

      - Typically very low context-switching overhead

    * Disadvantages:

      - Not necessarily backwards compatible

      - Typically worse performance since most type-safe languages are relatively slow

      - Usually garbage collected, so hardware to control memory layout and execution characteristics

## In groups

Take the example you had of something that _is_ an operating system, and
discuss what category of isolation mechanisms it uses and how.

# Conclusion

  * "Operating systems" covers a broad range of systems for our purposes

  * Exploring the trade-off between extensibility, performance, and safety

  * Each time: what is the isolation mechanism? What is the API?

Reading assignments:

  * "The Slow Winter" - James Mickens

  * "The Design of the Venus Operating System" - Barbara Liskov

