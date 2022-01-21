---
title: "What is software architecture?"
categories:
  - Blog
tags:
  - MISC
---

We all know that software architecture is something somewhat important for every software, even the simples one.

But still, there is one question: what is Software Architecture?
There's not a unique definition.

The [standard ISO/IEEE 42010](https://www.iso.org/obp/ui/#iso:std:iso-iec-ieee:42010:ed-1:v1:en) defines architecture as 

> Fundamental concepts or properties of a system in its environment embodied in its elements, relationships, and in the principles of its design and evolution

This definition has some implications:

* it is fundamental
* it refers to properties of a system, not to details
* it's about relationships between elements
* it can evolve

More in general, SA is about the definition of structures, where each structure can consist of one or more elements. When all the structures work together, you will have a working super-structure that works as expected.

Architects can/should ignore the implementation details of an element: the fundamental part is the communication between structures - how all the stuff fits together.

Good architecture must consider the long-term implications of the design, as well as the quality and the usefulness of every element.
As usual, early decisions are the most difficult ones to revert: architects should be smart and define a structure that may evolve and adapt to new requirements.

So, architects must focus on

* definition of elements and communication
* requirements (functional and non-functional)
* possibility of architecture evolution
