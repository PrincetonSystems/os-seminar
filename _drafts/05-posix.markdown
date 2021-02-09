
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

