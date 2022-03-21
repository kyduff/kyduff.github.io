---
layout: post
title: "The Use of Knowledge"
date: "2022-03-21"
categories: thoughts
published: true
---
My mind has been occupied by Hayek's [_The Use of Knowledge in Society_][hayek] for the past 3 days.

The focal premise of the article is that we ought to conceive of planning problems as problems of coordinating specialized (and individually incomplete) knowledge clusters instead of determining optimal solutions from a position of complete information. In Hayek's words:

> The problem is thus in no way solved if we show that all the facts, if they were known to a single mind (as we hypothetically assume them to be given to the observing economist), would uniquely determine the solution; instead we must show how a solution is produced by the interactions of people each of whom possess only partial knowledge.

I agree with Hayek's pivotal assumption, which is that a single actor is incapable of possessing complete knowledge of an economic system at every level of granularity. I admit that China's success as a surveillance state supports the claim that _sufficiently_ detailed knowledge may be obtained to allow central planning, though I'm not convinced this is optimal. It seems impossible to me that a central agent may possess all the information of a system, which is a belief I base on a heuristic assumption that the whole intelligence of any system must (in principle) exceed the intelligence of any part (I find that Buckminster Fuller's concept of [synergy] crops up a lot these days).

Regardless of belief, the planning problem boils down to the following minimax optimization:
1. Maximize coordination
2. Minimize dilution

A point Hayek harps on is that the planning problem is less about strategy and more about coordination. For macro scale growth we require some amount of coordination in the form of alignment to a plan that remains coherent over time (which allows gains to compound). The natural approach to this is to allocate a central planner to enforce a coherent plan, but the salient point of Hayek's article is that this accrues knowledge dilution risk; in other words, it ignores the second half of the minimax planning problem.

Dilution in this context refers to the lossy compression of local expertise which occurs in the communication channel between localized clusters of knowledge in an economic system. In particular, local knowledge is degraded when summarized for and aggregated by a central planner. An analogy is that the mean and variance insufficiently describe most abnormal distributions, and, for example, a central planner who approximates a distribution by a normal one and therefore neglects the kurtosis of the underlying distribution may undervalue tail risk and thereby expose the system to potential damage.

I think this idea is what Hayek was trying to get at when he wrote

> the sort of knowledge with which I have been concerned is knowledge of the kind which by its nature cannot enter into statistics and therefore cannot be conveyed to any central authority in statistical form ... It follows from this that central planning based on statistical information by its nature cannot take direct account of these circumstances of time and place, and that the central planner will have to find some way or other in which the decisions depending on them can be left to the "man on the spot."

### Summary

In the end, the things that stick are that:
* we operate in a macroeconomic system with fractured clusters of locally precise knowledge, each one's information being incomplete
* an optimally planned system will maximize coordination between these clusters while minimizing dilution of their expertise

### Beyond Economic Planning

Modelling systems in this way has made me think of tons of other applications, and I'm still clarifying my thoughts about them. I may write about it later, but in the meantime, here's a list of other stuff this article made me think about:
* the success of [garden farming][garden_farming] to the growth of east Asian agricultural economies in the 20th century (Joe Studwell talks about this at length in the first part of his book [How Asia Works][how_asia_works])
* the potential trajectory towards AGI via [modular intelligences that communicate][modular_intelligence]
* [John Boyd][boyd] and the comparative importance of [responsiveness rather than raw power in combat][ooda]
* the insane success of the internet's decentralized routing protocol
* [the pattern of history's greatest CEOs as capital allocators rather than micromanagers][outsiders]
* autonomy granted to researchers at [Xerox PARC under Bob Taylor's direction][dream_machine]

[hayek]: https://www.kysq.org/docs/Hayek_45.pdf
[synergy]: https://en.wikipedia.org/wiki/Synergetics_(Fuller)
[garden_farming]: https://en.wikipedia.org/wiki/Market_garden
[how_asia_works]: https://www.amazon.com/How-Asia-Works-Joe-Studwell/dp/0802121322/ref=sr_1_1?crid=CJCYSGMAZGPP&keywords=how+asia+works&qid=1647860267&sprefix=how+asia+wor%2Caps%2C255&sr=8-1
[modular_intelligence]: https://www.fhi.ox.ac.uk/wp-content/uploads/Reframing_Superintelligence_FHI-TR-2019-1.1-1.pdf
[boyd]: https://en.wikipedia.org/wiki/John_Boyd_(military_strategist)
[ooda]: https://thestrategybridge.org/the-bridge/2016/8/16/a-new-plan-using-complexity-in-the-modern-world
[outsiders]: https://www.amazon.com/Outsiders-Unconventional-Radically-Rational-Blueprint/dp/1422162672
[dream_machine]: https://www.amazon.com/Dream-Machine-M-Mitchell-Waldrop/dp/1732265119/ref=sr_1_1?crid=3OH99VFRGFHNW&keywords=the+dream+machine&qid=1647860419&sprefix=the+dream+mach%2Caps%2C216&sr=8-1
