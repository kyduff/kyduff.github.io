---
layout: post
title: "Information Processing Inequality"
date: 2021-08-19 12:00:00 -0700
categories: proofs
published: false
---

Being involved with data science, I think about the conceptual implications of the information processing inequality all the time. A particular subcase tells us that you can't "inject" information by performing some kind of transformation. Here are the details.

Random variables $X, Y, Z$ with nontrivial probability mass functions form a _Markov chain_ if

$$
p(x,y,z) = p(z|y)p(y|x)p(x).
$$

In this case, we write $X \to Y \to Z.$

_Lemma._ If $X \to Y \to Z$, then $X \perp Z$ given $Y$, that is, $X$ and $Z$ are _conditionally independent_ given $Y$.

_Proof._ This can be obtained from algebraic manipulation. 

$$p(x,y,z) = p(x,z|y)p(y),$$

and also

$$p(x,y,z) = p(x)p(y|x)p(z|y) = p(x|y)p(z|y)p(y)$$

since $X \to Y \to Z$. $Y$'s probability mass function being nontrivial allows us to cancel and obtain $p(x,z\|y) = p(x\|y)p(z\|y)$ as desired. $\Box$

We are now prepared to prove the main result.

_Theorem (Information Processing Inequality)_. If $X \to Y \to Z$, then

$$ I(X;Y) \geqslant I(X;Z). $$

In other words, $Y$ shares at least as much information with $X$ as does $Z$.

_Proof._  First we expand $I(X;Y,Z)$. Since $X \perp Z$ given $Y$, $I(X;Z\|Y) = 0$, therefore

$$
\begin{align*}
I(X;Y,Z) &= I(X;Y) + I(X;Z|Y) \\
&= I(X;Y).
\end{align*}
$$

On the other hand, $I(X;Y,Z) = I(X;Z) + I(X;Y\|Z)$. Since mutual information is non-negative, it follows that $I(X;Y) \geqslant I(X;Z)$. $\Box$

So why is this important? A particular case of interest is the following: notice that $X \to Y \to g(Y)$ for any function $g$. The information processing inequality then tells us that $I(X;Y) \geqslant I(X;g(Y))$ (for _all_ functions $g$). Heuristically, this means if you have some process $Y$ which shares information with a target process $X$, no transformation made upon $Y$ can make $Y$ share _more_ information with $X.$

Changing notation a bit, the statistical relevance become apparent. Suppose that a family of distributions $\\{\mathbb{P}\_\theta\\}$ is parameterized by a (random) variable $\theta$. Now suppose $X$ is a random matrix whose rows are samples from $\mathbb{P}\_\theta$. Let $f$ be a statistic computed on $X$, which might be a linear model, a normalization, a forward pass in a neural network, &c. It follows that $\theta \to X \to f(X)$ and that $I(\theta; f(X))\leqslant I(\theta; X)$. Hence, $f$ can only _reduce_ the mutual information of $X$ with $\theta$. This gives us a formal way of saying that

> _the magic is in the data_.

Philosophically this supports the compression model of neural networks in the sense that a neural network has the capability to _distill_ information, but it cannot _create_ information. The only available novelty is a fresh recombination of pre-existing components. Some might say this presents a barrier between man and machine insofar as man can create "genuinely," whereas machines are limited to recollection. But after reflecting on this, I have found that human ingenuity consists entirely of (albeit sometimes unlikely) recombinations. After all, the beauty of our world is a mere recombination of ancient atoms.

Back to Earth. Practically, this means if you start with crappy data you're going to get crappy results, _so focus on the data_.