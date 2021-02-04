---
slug: monolithic-kernels
number: 3
title: To UNIX or not to UNIX?
---

Monolithic Kernels
==================

  * "Application" code sandboxed, everything else in ring-0

  * Kernel bakes in all OS abstractions and, therefore, device drivers, multiplexing layers, APIs etc.

  * Vs. a microkernel where abstractions and drivers are run in protected "services"

  * Which kind is Linux/Windows/OS X?

UNIX
====

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

  * Shells as extensibility

    - Git!

    - Why not a process for each command?

  * "Evaluation"

    - 14 maximum users

    - 4.3 CPU hours per day (0.17%)

    - 98% uptime (1/3rd faults from software)

POSIX Paper
===========

  * Background

    - Authors:

      * Roxana Geambasu: security/privacy in distributed systems and mobile (Pebble)

      * Jason Nieh: virtualization & cross-executing iOS apps on Android (Cider)

      * Jeremy Andrus: now a kernel engineer at Apple

    - POSIX? Portability across UNIX-like systems

    - Modern user-facing apps:

      * Highly structured data

      * Data stored in structured files in file system (SQLite)

      * Rich graphics, access to specialized devices

    - Personal computers different from PDP-11?

      - More devices? More performance sensntivie?

    - Modern OSs:

      - Flavors of Linux

      - Flavors of Android

  * What are the high level conclusions?

    - ioctl is one of the most used system calls... it's the "other" system call, so implies POSIX is not sufficient.

      - Graphics, Networking, IPC

    - Why was this not a problem until now?

    - Does this extend to other uses of Linux? E.g. networked servers?

    - What does this say about the cost of UNIX's abstractions/extensibility mechanisms?

  * To what extent is this an artifact of a monolithic kernel architecture?

