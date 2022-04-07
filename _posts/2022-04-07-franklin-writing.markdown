---
layout: post
title: "Franklin the Writer"
date: "2022-04-07"
categories: thoughts
published: true
---
As a teenager, Benjamin Franklin would sneak writing samples under the door of his brother’s printing shop, hoping they’d find their way into the _The English Courant_—the shop’s major news publication. He later became famous for writing _Poor Richard’s Almanac_, several treatises on natural sciences, and countless diplomatic letters. He says of himself:

> Prose writing has been of great use to me in the course of my life, and was a principal means of my advancement.

Franklin attributes his writing ability to deliberate effort put towards its improvement. This began after Franklin's father commented on a series of his teenage letters that while "[Franklin] had the advantage of [his] antagonist in correct spelling and pointing (which [he] ow'd to the printing-house), [he] fell far short in elegance of expression, in method, and in perspicuity."

From this, Franklin sought to improve his writing with a collection of regularly practiced tasks. Here they are:

_Reconstruction._

> About this time I met with an odd volume of the _Spectator_ … I bought it, read it over and over, and was much delighted with it. I thought the writing excellent, and wished, if possible, to imitate it. With this view I took some of the papers, and, making short hints of the sentiment in each sentence, laid them by a few days, and then, without looking at the book, try'd to compleat the papers again, by expressing each hinted sentiment at length, and as fully as it had been expressed before, in any suitable words that should come to hand. Then I compared my _Spectator_ with the original, discovered some of my faults, and corrected them.


_Prose to poetry and back._

> I found I wanted a stock of words, or a readiness in recollecting and using them, which I thought I should have acquired before that time if I had gone on making verses; since the continual occasion for words of the same import, but of different length, to suit the measure, or of different sound for the rhyme, would have laid me under a constant necessity of searching for variety, and also have tended to fix that variety in my mind, and make me master of it. Therefore I took some of the tales and turned them into verse; and, after a time, when I had pretty well forgotten the prose, turned them back again.


_Reorganization._

> I also sometimes jumbled my collections of hints into confusion, and after some weeks endeavored to reduce them into the best order, before I began to form the full sentences and compleat the paper. This was to teach me method in the arrangement of thoughts. By comparing my work afterwards with the original, I discovered many faults and amended them; but I sometimes had the pleasure of fancying that, in certain particulars of small import, I had been lucky enough to improve the method of the language, and this encouraged me to think I might possibly in time come to be a tolerable English writer, of which I was extremely ambitious.


### Some thoughts

It’s interesting how similar these are to modern techniques of pre-training machine learning language models.

For example, the fundamental contribution of [BERT] (which broke 11 records and became one of the most influential language models of all time) was a pre-training technique wherein the model was forced to reconstruct groups of words that had been omitted from a body of text. This isn’t the same as Franklin’s reconstruction task, but it’s similar. In machine translation, one of the most common pre-training techniques is called "back translation" where a source language is translated into a target language and then back again and compared to the original. This is obviously very similar to Franklin’s poetry task.

I wonder what other learning techniques we might devise by studying the way machines learn.



[BERT]: https://arxiv.org/abs/1810.04805