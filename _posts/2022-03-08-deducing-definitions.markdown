---
layout: post
title: "Deducing Definitions"
date: "2022-03-08"
categories: thoughts
published: true
---
I started writing something about necessary yet insufficient descriptions of complex problems and gave it the title "What Makes an Apple Pie?", but in my difficulty composing that essay, I decided that a more apt approach to my first entry in _Thoughts of The Day_ would directly address something to do with formalizing thoughts. Maybe one day you’ll learn what makes an apple pie, but today is not the day I tell you.

What I’m going to do is write a short piece describing the process I use to define problems and make decisions based on formal reasoning. Why? I want my first essay to have a few properties:
* it shouldn’t be long enough to set a trend of lengthy rants in this column (though I plan to allow my entries to stretch as far as they can retain content)
* it should be about something I’m extraordinarily familiar with so that it’s easy to write
* it should be embarrassing enough to make me comfortable publishing organic content in future essays

So let’s get into it. Claude Shannon defined entropy by first conceiving of a concrete notion of "surprise" and concluding that an appropriate mathematical definition capturing the concept should have the following three properties:
* events which are improbable should also be surprising
* your surprise at two independent events happening together should be the sum of the surprises of seeing each event independently
* surprise should increase continuously with improbability

From here you can use some mathematics to show that the logarithm function is the only function satisfying these properties, and hence the definition of "information" was born. Clearly this definition worked very well, because Claude Shannon rode it into a life of fame and leisure as information theory grew into the basis for all modern digital communication. So what went on here? How did Shannon come up with this definition? Crucially, Shannon didn’t start with his definition and then deduce properties. He started with the _properties_, and then _deduced_ his definition. This is an application of the wider trend in mathematics to "work backwards," which is a tactic advocated by most of history’s greatest problem solvers.

I find decisions often consist of defining a course of action, therefore I tend to approach decisions similarly to how I would approach making mathematical definitions. In particular, I like to make lists that answer questions:
* what properties do I want?
* what should my answer _do_?
* what is necessary?
* how should my answer interact with other things?

An underrated side effect of this approach is that if you develop these lists in collaboration with other people, you very naturally develop a canonical language that enables more effective discussions while evaluating alternatives. If the objectives and criteria are developed with organic and transparent consensus from the beginning of the decision making process, it makes it much easier to express opinions that will be respected and understood as intended.