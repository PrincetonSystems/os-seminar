---
slug: adminitrativia
number: 2
title: Going over the syllabus
---

# Syllabus Overview

## Deliverables

  1. Asynchronous paper discussions (on Perusall)
  2. In person discussions
  3. Term project

### Asynchronous paper discussions

For each paper, five (5) substantive comments?

  * A critique
  * Background information learned outside the text
  * Questions or points for discussion
  * A response to someone else's question
  * ...

This should be easy if you're reading the paper in preparation for a class discussion.

Read the paper _at least_ twice:

  1. What is the paper about? What are the authors trying to argue or show?

     1. When was the paper written?
     2. Who are the authors?
     3. What kinds of work do they cite?
     4. Read the introduction, then the conclusion, then try to infer what you'll see in the body of the paper.
     5. Read the body of the paper at a high level (without getting too fixated on details).

  2. OK, time to read in depth.

     1. What are the authors asking you to make? Are they reasonable? If the
        assumption are wrong (or not-applicable), does their argument still
        hold water?
     2. What assumptions _must_ you make, even though the authors don't say so explicitly?
     3. What claims does the paper make that _must_ be supported?
         * Is it in the citations?
         * Is there an evaluation? A proof sketch? Etc...
     4. How do they support the main arguments?
         * Design makes arguments true by construction?
         * Performance evaluation?
         * How is "extensibility" **measured**? (example applications, user study, established benchmarks?)

### In person discussion

Assuming you've made at least 5 substantive comments, you just have to show up
and put in a good faith effort to move the discussion forward. The goal of the
discussions is to have a higher bandwidth discussion about either points raised
on Perusall or points related specifically to the theme of the course.

## Term Project

**tl;dr**: You must submit a 6-page (USENIX-style) paper alonge or in groups on
a project of your choosing related to the course theme.

The main graded component (40%) of the class is a term project, roughly
equivalent to a workshop submission or the literature review section of a
thesis. These can be done along, or in groups, and involve four deliverables:

1. 1-2 page proposal, due March 9th
2. Proposal presentation (~10 minutes per project) on March 18th & 23rd
3. A 6-page (USENIX-style) report due on Dean's day (May 4th)
4. Final presentation, in the last few class meetings (depending on the number of projects)

Projects can be:

* Building a system that explores some point on the extensibility, performance, security triangle
* _Deeply_ evaluating an existing system using this framework
* A literature review on a particular topic related to the framework (e.g.,
  language-based isolation techniques used to run untrusted distributed
  computations).
* Convince me!

Part of your task is to scope the project wisely. If you are building a system,
what can you reasonably do in a couple months? Is there a prototype version or
proof-of-concept that gives you enough to evaluate? Is there a component of the
whole system is sufficient?

## Rough schedule of readings:

1. Kernels:
   1. Monolithic
   2. Micro-
   3. Extensible-
   4. High performance
2. Distributed systems
3. Language-based isolation
4. Networking
5. Misc. if we get to it

# Venus

## Barbara Liskov

  * Turing Award
  * First woman to get a PhD in computer science in US
  * Early work in OOP
  * Formalized subtyping
  * Promise pipelining
  * Viewstamp replication
  * PBFT

## Historical Context

  * Third ever SOSP (the only Operating Systems publicaion venue until 1994)
  * Circa 1970
  * "Minicomputers" are the iPhone of the day.
    * Mini in contrast to mainframes. $1M vs. $10K, so many many more were available
    * Mainframes were typically batch-processed very literally: hand your program
      on cards to the mainframe operator, and they would ring you when your
      program had been run.
    * Minicomputers were typically interactive (e.g. many users connected via
      terminals), so time-sharing systems were necessary.
  * Hardware/software co-design is the norm, for decades to come. Most OS
    vendors (PDP, IBM, HP, VAX, Apple, Sun) also build the hardware, including CPUs.
    * The IBM PC in the 90s is the first real hardware "standard" (and still the one we know today).

## The Venus Machine

  * Timesharing system
  * 16 teletypes
  * One user per virtual machine

## Venus

  * How are users/processes isolated?
    * Memory?
    * Performance?
    * Other resources?

