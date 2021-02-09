---
slug: unix
number: 3
title: To UNIX or not to UNIX?
---

# Monolithic Kernels

  * "Application" code sandboxed, everything else in ring-0

  * Kernel bakes in all OS abstractions and, therefore, includes device
    drivers, multiplexing layers, APIs, scheduler etc.

  * Contrast with a microkernel where abstractions and drivers are run in
    protected "services" sandboxed in userspace.

  * Which kind is Linux/Windows/OS X?

# UNIX

  * Characteristics of the PDP-11

    - What's new, what's different?

      * 144KB RAM, 20MHz, 1MB native storage

      * Handful of devices?

  * What about UNIX is more/less "extensible" than Venus?

  * Ability to share reentrant code. What does this mean?

    - Basically no globals

  * "The most important job of UNIX is to provide a file system"

  * Special files, pros & cons of read/write interface

    - fseek?

    - Multiplexing?

    - Locks?

  * UNIX permissions and ACLs

    - What are the kinds of policies that we can reason about?

    - "the system recognizes one particular user ID (that of the "super user")
      as exempt from the usual constraints on file access."

  * Pipes

    - No deadlock because pipes can't be circular

  * "Evaluation"

    - 14 maximum users

    - 4.3 CPU hours per day (0.17%)

    - 98% uptime (1/3rd faults from software)

# Discussion Points to touch on

  * File system a central part of the OS

     * Role: abstract storage device?

  * The userspace shell & economy of mechanism

  * Design choices, extensibility vs performance vs security:

    * File name length

    * Tree structure

    * No hard links to directories

    * Expose every device as file(s)

    * `setuid`

    * Semantics of fork

    * Namespacing (file system roots, PATH)

  * Building and OS for fun rather than profit

