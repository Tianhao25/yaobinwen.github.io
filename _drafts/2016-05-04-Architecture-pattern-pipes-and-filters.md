---
layout: draft
title: Architecture Pattern: Pipes and Filters
date: 2016-05-04
comments: true
category: Essay
tags: [architecture][pipe-and-filter]
description: The introduction and analysis to the architectural pattern "Pipes and Filters", as well as a concrete example.

---

## Semantics

Let's look at the semantics of the Pipes and Filters pattern.

**1). No knowledge of upstream/downstream filters.**

The key point here is: The shared knowledge will harm the independence of the filters and make their correctness dependent to one another.

We need to be clear about what it means by "no knowledge". We know that a filter must write data to its output pipe in a specific format that contains a certain set of information so the downstream filter can parse it and get the input. The questions are:
* Is the "format" considered to be the knowledge shared between the filters? Such kind of information may be inevitable because some kind of "format" has to be defined as long as two parties want to communicate to each other. Without such predefined format, no communication could happen. Therefore, it is not considered as the shared knowledge.
* Are the information fields contained in the data passed along the pipes considered to be the knowledge shared between the filters? No, because such information is the input of the next filter. It is necessary for the downstream filters to work correctly.

**2). The system should not depend on the scheduler.**
