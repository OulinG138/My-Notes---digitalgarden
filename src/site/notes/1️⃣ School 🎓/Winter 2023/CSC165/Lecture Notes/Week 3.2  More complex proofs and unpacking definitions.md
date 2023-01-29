---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-165/lecture-notes/week-3-2-more-complex-proofs-and-unpacking-definitions/","dgPassFrontmatter":true}
---

## Proofs
> Prove that for all integers $x$, if $x$ divides $(x+5)$ then also divides $5$.
1. Told to prove
2. $\forall x \in \mathbb{Z}, x \mid (x+5) \Rightarrow x \mid 5$ or $\forall x \in \mathbb{Z}, (\exists k_1 \in \mathbb{Z}, x+5 = k_1x) \Rightarrow (\exists k_2 \in \mathbb{Z}, 5 = k_2x)$
3. Try some concrete values of $x$
$\text{Try } x = 5$
- $\text{LHS of equal sign in the hypothesis}$
$$
\begin{align}
	x + 5 &= 5 + 5 \\
	 &= 10 \\
	 &= 2 \cdot 5 \\
	 &= 2 \cdot x \\
	 &= k \cdot x \text{ for } k = 2
\end{align}
$$
$\text{So } x \mid (x+5), \text{hypothesis of } \Rightarrow \text{True}$
- $\text{RHS of equal sign}$
$$
\begin{gathered}
\text{Want to show } x\mid 5 \\
\text{True since } 5 = 1 \cdot 5 \text{, so } 5 \mid 5 \\
\text{when } x= 5,x \mid (x+5)\Rightarrow x\mid 5 \text{ is True}
\end{gathered}
$$
4. Consider $x =10$
$$
\begin{align}
x \mid (x+5) \Rightarrow x\mid 5 \text{ is True}
\end{align}
$$
- In the case that $x=10$, it is vacuously True.

5. Consider $x=1$
$$
\begin{align}
	 &= 1 + 5 \\
	 x+5&= 6 \\
	 &= 6 \cdot 1 \\
	 &= k \cdot 1 \text{ for } k = 6
\end{align}
$$
$\text{So } x \mid (x+5), \text{hypothesis of } \Rightarrow \text{True}$
- $\text{RHS}$: $1\mid 5$ is True, $5=k\cdot 1 \text{ for } k = 5$
---
- **Observed**
	- If LHS of implication is False, statement is vacuously True.
	- If LHS of implication is True, need to prove RHS of implication is true to prove implication.
$\text{We know } x \mid (x+5), x+5 = kx \text{ for some } k \in \mathbb{Z}$
$\text{To prove implication need to show } x \mid 5, \text{ need to find a } k_{2} \text{ s.t. } 5=k_2x$
$$
\begin{align}
	 x+5&= kx \\
	 5&= kx -x \\
	 &= (k-1)x
\end{align}
$$
$$\begin{gather}\text{so } \exists k_{2}\in \mathbb{Z}, 5 = k_2x\end{gather}$$
- **Proof**
	- $\forall x \in \mathbb{Z}, x \mid x+5 \Rightarrow x\mid 5$
$$
\begin{gather}
\text{Let } x \in \mathbb{Z}\\
\text{And assume } x\mid (x+5)\\
\text{That is, } \exists k_{1}\in \mathbb{Z}, x+5 = k_1x\\
\end{gather}
$$
$$
\begin{align}
x+5 &= k_{1x}\\
\text{then } 5 &= k_1x-x\\
&= (k_{1}-1)x\\
\text{Let } k_{2}&=k_{1}-1\\
\text{then } 5 &= k_2x\\
\text{and } \exists k_{2}\in \mathbb{Z}, 5&=k_2x
\end{align}
$$

&nbsp;

### Prove general statement above
- Exploring a prime predicate:
$Prime(p): p > 1 \land (\forall d \in \mathbb{N}, d\mid p \Rightarrow(d=1 \lor d=p)), \text{ where } p\in \mathbb{N}$
- Consider:
$\forall p \in \mathbb{N}, \forall x \in \mathbb{N}, (Prime(p) \lor x\mid (x+p) \Rightarrow (x=1 \lor x=p))$
 1. Try to prove true
 2. given
 3. Suppose $p_{1}x \in \mathbb{N}$
 $$
\begin{gather}
\text{Assume } Prime(p) \\
\text{and } x\mid (x+p)\\
\text{want to show } x=1 \text{ or } x=p
\end{gather}
$$
$\text{From an earliear work today, } x\mid (x+p) \Rightarrow x\mid p$
$\text{Since } p \text{ is prime, we know } x=1 \text{ or } x=p \text{ since advisor of a prime number is either } 1 \text{ or iteself.}$
4. Proof.
$$
\begin{gather}
\text{Let } p, x \in \mathbb{N}\\
\text{Assume } p \text{ is prime and that } x\mid (x+p)\\
\text{Since } \forall d \in \mathbb{Z}, \forall x \in \mathbb{Z}, x\mid (x+d) \Rightarrow x \mid d\\
\text{We can conclude that } x\mid p
\end{gather}
$$
$\text{Since } p \text{ is prime}, \text{ its only divisors are } 1 \text{ or } p, \text{ so we can conclude that } x=1 \text{ or } x=p$
