---
layout: page
title: SyGuS-Comp 2019
icon: medal
sidebar_link: true
sidebar_sort_order: 200
---

The 6<sup>th</sup> Syntax-Guided Synthesis Competition (SyGuS-Comp)
will take place as a satellite event of CAV and SYNT 2019.


### Important Dates

<div class="dates" markdown="1">

|------------------|---------------------------------------------------------------------------------|
| 1 May 2019       | Deadline for submitting benchmarks                                              |
| 1 June 2019      | Deadline for submitting the first version of solvers                            |
| 14 June 2019     | Deadline for submitting the final version of solvers and their descriptions     |
| 7 July 2019      | Notification of results to authors                                              |
| 13/14 July 2019  | Solvers presentation (at SYNT'19 workshop)                                      |

</div>


### Call for Participation

This is a call for participation in the 6<sup>th</sup> Syntax-Guided Synthesis Competition
to be organized as a satellite event of SYNT and CAV 2019 to be held in New York City.

The classical formulation of the program-synthesis problem is to find a program
that meets a correctness specification given as a logical formula.
Recent work on program synthesis and program optimization illustrates many
potential benefits of allowing the user to supplement the logical specification
with a syntactic template that constrains the space of allowed implementation.
The motivation is twofold.
First, narrowing the space of implementations makes the synthesis problem more tractable.
Second, providing a specific syntax can potentially lead to better optimizations.

The input to the syntax-guided synthesis problem (SyGuS) consists of a background theory,
a semantic correctness specification for the desired program given by a logical formula,
and a syntactic set of candidate implementations given by a grammar.
The computational problem then is to find an implementation from the set of candidate expressions
that satisfies the specification in the given theory.
The formulation of the problem builds on SMT-LIB.

There has been a lot of recent interest in both using SyGuS solvers for various synthesis applications
and developing different solving algorithms.
The SyGuS competition (SyGuS-Comp'19) will allow solvers to compete on a large collection of benchmarks
and advance the state-of-the-art for program-synthesis tools.
We invite authors to submit their SyGuS solvers to this year's SyGuS Competition.

For questions regarding the competition please contact the organizers at <sygus-organizers@seas.upenn.edu>.


### Competition Tracks

This year's competition will have 5 tracks:
<br>
- General SyGuS track (_General_),
- Invariant synthesis track (_INV_),
- Conditional Linear Integer Arithmetic track (_CLIA_),
- Programming By Examples [Theory of Strings] track (_PBE-Strings_), and
- Programming By Examples [Theory of Bit Vectors] track (_PBE-BV_).

Check the [specification language](/language) for more details
on the formulation of the problems for these tracks.

**NOTE:**
This year's SyGuS competition will use a lightly-modified version of the SyGuS input format
that was used in previous competitions.
The new format is more compliant with SMT-LIB version 2.6,
includes minor changes to the concrete syntax for commands,
and eliminates several deprecated features of the previous format.

A comprehensive description of the new input format
and its differences with respect to the previous format
is available in the reference document "[_The SyGuS Language Standard Version 2.0_](/assets/pdf/SyGuS-IF_2.0.pdf)".


### Evaluation

Solvers will be evaluated on the [StarExec] platform,
which provided 200 dual quad-core machines with 256GB memory each.
The solvers would be run with a _TIMEOUT_ value.
The SyGuS-correctness checker, as well as the solvers from last year's competition
are available on the SyGuS community at StarExec.
Candidate participants are invited to register on StarExec,
where they can easily compare their solvers to the previous ones against the public benchmarks.


### Scoring Scheme

The scoring system is per track and as follows.
<br>
A solver that solved $$ N $$ benchmarks in the track, out of which $$ F $$ benchmarks among the fastest[^1], and
$$ S $$ benchmarks with an expression size among the smallest[^2] will receive a score: $$ 5 N + 3 F + S $$.
The solver with highest score will be announced the winner of the track.


### Tool Submission and Description

We expect tool developers to test their solvers on the public benchmarks,
and submit the solver binaries on StarExec by the solver submission deadline.
Each solver submission should also be accompanied by a brief (1 -- 2 page in IEEE format)
description of the key ideas of the solver.


### Licensing of Tools and Benchmarks:

All benchmarks will be made public after the competition.
We encourage the tool developers to make their solvers open-source,
but participants are welcomed to submit binaries of proprietary tools as well.


[^1]: according to the pseudo-logarithmic time scale used in previous competitions
[^2]: according to the pseudo-logarithmic size scale used in previous competitions

{% include common_links.md %}
{% include common_abbrv.md %}