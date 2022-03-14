---
layout: post
title: "Post Quantum Scaling I"
date: "2022-03-14"
categories: thoughts
published: true
---
Quantum computing poses a threat to security protocols underlying the modern internet, but it doesn't have to pose a threat to the future's internet.

What's the problem? Modern security protocols rely on the difficulty of factoring many-digit [semiprime] numbers.[^1] In particular I'm talking about cryptographic signatures. Cryptographic signing is built on the premise that I can display a public identifier key linked to a private "signing key" so that counterparties can verify that—without revealing the value of the private signing key—indeed _I_ signed a message using the private key linked to my public identifier. In practice this is implemented with large semiprime numbers (along with some other [math magic][magic]), though its implementation admits a method to compute the private key associated with a given public key, given that semiprime numbers can be factored efficiently.

Quantum computers with sufficiently many stable qubits[^2] can do this time-efficiently. From here the substance of this is derived from the inevitability of practical factoring systems: it’s not a matter of whether physically implemented quantum computers will crack digital signature algorithms, but when. My impression is that modern crypto systems will only survive in their current form if funding for quantum computing research dries up. This I think is unlikely, at the very least because quantum computers are effective simulators for chemical phenomena relevant to drug discovery.

# Attack Surface 1: Blockchains

Positing the existence of stable quantum computers with many (many) qubits, what is the attack surface of modern blockchains? I’ve already mentioned vulnerabilities in the private/public key pair system. Another problem is zk-proofs.

## The Problem With Proofs

Most Ethereum scaling solutions rely on zero knowledge proof (zk-proof) systems to securely compress a computation into a public commitment that is easier to validate than it is to perform the underlying compute task. There are three systems that dominate this task:
* SNARKS
* STARKS
* Bulletproofs

What matters in the context of this post is that SNARKS and Bulletproofs are susceptible to quantum threats whereas STARKS are (so far) believed immune. Despite their vulnerability to quantum attacks, SNARKS are used the most in practice by a wide margin. Why? The short answer is space efficiency (and the long answer would address tooling and history): regardless of the size of computation, SNARKS take up 288 bytes whereas STARKS take up ~45,000 bytes and scale with computation size like $O(p(\log n))$ for a polynomial $p$.

In the current environment of high Ethereum gas fees, the extra 2 orders of magnitude are very costly. A SNARK can fit into a transaction absorbing ~600k gas, whereas STARKS soak up nearly 2.5 million gas. At current gas prices (roughly $37 \times 10^{-9}$ ETH / gas), that’s a difference of roughly USD 1700 for each zk-proof. As a solution to a problem that doesn't exist yet, it's a tough sell.

So what can we do? The quantum threat is inevitable and requires attention sooner than later. Post-quantuming crypto systems is going to be harder than it seems, so we should get started as soon as possible. For STARKS to be adopted, either their size needs to be reduced substantially or they need to be deployed on a chain with lower gas fees. Doing the former seems harder to me.

The tech behind STARKS is new and exciting. It would be great to see more people working on compressing the STARK (or another post-quantum zk system) footprint so we can make steps towards a future version of the internet that will survive the birth of quantum computing at scale.

---

[^1]: For the curious: most security protocols (including those underlying Bitcoin and Ethereum) don’t actually use natural numbers but rather an algebra of numbers whose multiplicative operation is derived from bouncing points around on an elliptic curve. This is done because the same security level (measured in difficulty to crack) requires almost 10x more bits in classical RSA than in the elliptic curves version. If you’re interested, check out [ECDSA].

[^2]: Fortunately the number of required qubits is [quite high][qubits].

[semiprime]: https://en.wikipedia.org/wiki/Semiprime
[ECDSA]: https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm
[magic]: https://en.wikipedia.org/wiki/RSA_(cryptosystem)
[qubits]: https://research.kudelskisecurity.com/2021/08/24/quantum-attack-resource-estimate-using-shors-algorithm-to-break-rsa-vs-dh-dsa-vs-ecc/

