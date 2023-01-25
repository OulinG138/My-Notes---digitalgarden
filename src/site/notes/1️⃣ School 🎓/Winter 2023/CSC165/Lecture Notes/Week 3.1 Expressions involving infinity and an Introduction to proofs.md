---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-165/lecture-notes/week-3-1-expressions-involving-infinity-and-an-introduction-to-proofs/","dgPassFrontmatter":true}
---

## Recap Example
```ad-faq
title: How could we express “There are infinitely many even numbers?”


- How many integers are there?
	- Infinitely many.
- How do we know?
	- If there were finite many, then we could call the biggest integer $B$.
	- Add $1$ to $B$ we have $B+1$, and $B+1>B$. So $B$ cannot be the largest integer. This contradicts the original assumption, so we can conclude that there are infinitely many integers.


- Every integer has another integer larger than it.
	- $\forall x \in \mathbb{Z}, \exists y \in \mathbb{Z}, y > x$
- Every number has an even number that is larger than it.
	- [x] $\forall x \in \mathbb{Z}, \exists y \in \mathbb{Z}, 2y > x$
	- [x] $\forall x \in \mathbb{Z}, \exists y \in \mathbb{Z}, Even(y) \land y > x$
	- [ ] $\forall x \in \mathbb{Z}, \exists y \in \mathbb{Z}, Even(x) \land y > x$
```

&nbsp;

## Proofs
- **Proofs**: An argument that show that a statement is True.
- **Disproof**: An argument that shows that a statement is False.

### Start Writing Proofs
> **Statement:** Some power of two is greater than 1000.
1. Think is True since some powers of 2 grows to $\infty$
2. $\exists n \in \mathbb{N}, 2^{n} > 1000$ or $\exists n \in \mathbb{Z}, P(n) \text{ where } P(n): \text{``}2^{n} > 1000\text{"}, \text{ where } n \in \mathbb{N}$ (**Type**: An existentially quantified predicate)
3. Rough Work
	-  $n = 10, 2^{10} = 1024 > 1000$
		- Just need one value to prove existence.
4. Proof

$$
\begin{align*}
\text{Let } n &= 10 \\
\text{Then } 2^{n} &= 2^{10}\\
&=1024 \\
&>1000 \\
\end{align*} 
$$
$$
\text{Hence, } \exists x \in \mathbb{N}, 2^{x} > 1000
$$

----

>  **Statement**: Every real number $n$ bigger than $20$ satisfies the inequality $1.5n - 4 \ge 3$
1. Yes, since $1.5n - 4$ is equal to a line with positive slope. Try $n=40$, $1.5(40) - 4 = 56 \ge 3$
2. $\forall n \in \mathbb{R}, n > 20 \Rightarrow 1.5n - 4 \ge 3$
3. Rough Work
$$
\begin{align}
\text{Arbitrary }n &\in \mathbb{R} \\ 
\text{Assume } n &> 20 \\ 
1.5n &> 30 \\ 
1.5n - 4 &> 26 \\ 
&\ge 3
\end{align}
$$




4. Proof: 

$$
\begin{flalign}
\text{Let } n \text{ be an arbitrary real number.} && 
\end{flalign}
$$

$$
\begin{flalign}
\text{We can perform the following manipulation on the inequality:} &&
\end{flalign}
$$
$$
\begin{align*}
\text{Assume that } n &> 20 \\\\
\text{Since } n &> 20 \\ 
1.5n &> 30 \\ 
1.5n - 4 &> 26 \\ 
1.5n - 4 &\ge 3\\
\end{align*}
$$


