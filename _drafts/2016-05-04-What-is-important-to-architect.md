---
layout: draft
title: What is Important to a Software Architect?
date: 2016-05-04
comments: true
category: Essay
tags: [architecture]
description: What a software architect must know and do.

---

I think a software architect must know and do the following things.

**An architect must know the semantics of an architectural pattern.** The **semantics** of an architectural pattern includes its rules/structures/policies which make the pattern what it is. An architectural pattern promotes and inhibits certain systemic properties because of its semantics. An architect needs to know the systemic properties that are promoted and inhibited by different patterns in order to choose the ones that she wants the most for her problem.

**An architect must follow the semantics of an architectural pattern if she wants to benefit from the promoted systemic properties.** As mentioned above, the systemic properties are promoted or inhibited because of the pattern's semantics. If the semantics is violated, it is not guaranteed that the systemic properties that should be promoted are still promoted.

However, an architect may not always follow the semantics of an architectural pattern strictly because her problem at hand may be complicated and not a single architectural pattern can solve all aspects of it. In this case, the architect must modify the architectural pattern and create a variation. This is fine, but the architect must have a clear mind of what is modified, because the modified part, in other words, the parts that violate the architectural pattern semantics, may compromise the systemic properties that they originally promote. **The architect must evaluate the modification to make sure the modified architectural pattern can still meet requirements to the systemic properties.**

**An architect must learn the business context, and be sensitive to its changes.** The architecture of the system is developed in the context of the business and is assumed to serve the business needs. An architecture that is developed without taking the business context into account may result in one that looks supreme from a technical perspective but won't fit the business development. The business context determines some of the systemic properties that are the most important to the system which must be built into the architecture (the other one that determines the systemic properties is the technical constraints). The architect must know the business context the system will be working in, and try as best as possible to predict possible changes in the future in order to make the architecture adaptable to those changes.
