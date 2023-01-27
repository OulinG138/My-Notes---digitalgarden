---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-165/week-3-2-more-complex-proofs-and-unpacking-definitions/","dgPassFrontmatter":true}
---

## Recap
> Prove that for all integers $x$, if $x$ divides $(x+3)$ that $x$ also divides $5$.
1. Told to prove.
2. $\forall x \in \mathbb{Z}, x \mid (x+5) \Rightarrow x \mid 5$ or  $\forall x \in \mathbb{Z}, (\exists k_1 \in \mathbb{Z}, x + 5 = k_1x) \Rightarrow (\exists k_2 \in \mathbb{Z}, 5 = k_2x)$
3. Try some constant values of $x$
	- Try $x=5$
$$\text{LHS of  = in the hypothesis} $$
$$\begin{align} 
x + 5 &= 5+5\\
&=10 \\
&=2 \cdot 5 \\
&=2 \cdot x \\
&= k \cdot x \text{ for } k = 2 \\
\end{align}
$$
- So $x \mid (x+5)$, hypothesis $\Rightarrow$ True
- WTS $x \mid 5$
	- True since $5 = 1\cdot 5$
		- so $5 \mid 5$
- When $x=5$, $x \mid (x+5) \Rightarrow x\mid 5$ is True
- Consider $x = 10$
	- $x+5=10+5=15$
		- Does $10\mid 15$ ?
		- There is no $k \in \mathbb{Z}$, so that $15=k\cdot 10$ and so $10 not 15$
	- What can we say about it?
		- $x\mid (x+5) \Rightarrow x\mid 5$ in the case that $x=10$. So it is vacuously True.
- Let $x=1$
	- $1+5$ = $x+5 =6 = 6\cdot 1 =k \cdot 1$ for $k=6$
		- So hypothesis $m \Rightarrow$ is True.
		- Conclusion of $\Rightarrow$ $1 \mid 5$. Yes! $5=k\cdot 1$ for $k=5$

- Observed: 
	- If LHS implication is false, the statement is vacuously True.
	- If LHS of implication is True, then we need to prove RHS of implication is True to prove implication.
		- We know $x\mid (x+5)$, $x+5 = kx$ for some $k\in \mathbb{Z}$
			- To prove implication, we need to show $x\mid 5$, we need to find a $k_2$ s.t. $5=k_2x$
$$
\begin{align}
\text{Know } x+5&=kx\\
\text{So } 5&=kx-x\\
&=(k-1)x\\
\end{align}
$$
$$\text{So } \exists k_{2}\in \mathbb{Z}, 5=k_2x$$

1. Proof
- $\forall x \in \mathbb{Z}, x\mid x+5 \Rightarrow x\mid 5$
$$
\begin{align}
\text{Let } x &\in \mathbb{Z}\\
\text{And asssume } x&\mid (x+5)\\
\text{That is, } \exists k_{1}\in \mathbb{Z}, x+5=k_1x\\
x+5=k_1x
\text{then } 5 =k_1x-x\\
=(k_{1-1)x}\\
\text{Let } k_{2}= k_1-1\\
\text{then } 5 = k_2x\\
\text{and } \exists k_{2}\in \mathbb{Z}, 5 = k_2x\\
\text{That is } x\mid 5
\end{align}
$$
- Prove general statement above replacing 5's with d's


## An examples involving prime numbers
- Expanding a Prime predicate:
	- $\text{Prime}(P): P > 1 \land (\forall d\in \mathbb{N}, d \mid p \Rightarrow (d=1 \lor d=p))$, where $p \in \mathbb{N}$
- Consider
	- $\forall p \in \mathbb{N}, \forall x \in \mathbb{N}, (Prime(p) \land x\mid (x+p)) \Rightarrow (x=1 \lor x=p)$
		1. Try to prove true
		2. given
		3. Suppose $p, x \in \mathbb{Z}$
$$
\begin{align}
\text{Assume } Prime(p)\\
\text{and } x\mid (x+p)\\
\text{WTS } x=1 \text{ or } x=p\\
\end{align}
$$
- From an earlier work today
	- $x \mid (x+1) \Rightarrow x\mid p$
		- Since $p$ is prime, we know $x=1$ or $x=p$, since a divisor of a prime number is either 1 or itself.
- Proof
$$
\begin{align}
\text{Let } p, x \in \mathbb{N}\\
\text{Assume } p \text{ prime and does that } x\mid (x+p)\\
\text{Since } \forall d \in \mathbb{Z}, \forall x \in \mathbb{Z}, x\mid (x+d) \Rightarrow x\mid d\\
\end{align}
$$
- We can conclude that $x\mid p$
- Since $p$ is prime, its only divisor are $1$ or $p$.
- So we can conclude that $x=1$ or $x=p$   cvgfrt