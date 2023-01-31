---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-165/lecture-notes/week-4-1-proof-structure-and-an-alternate-charaterization/","dgPassFrontmatter":true}
---

## Back to $Prime$
- Consider the following predicate:
	- $Atomic(n): \forall a,b \in \mathbb{N}, (n \nmid a \land n \nmid b) \Rightarrow n \nmid ab$
- **Proving**
	- $\forall n \in \mathbb{N}, (n > 1\land Atomic(n)) \Rightarrow Prime(n)$
$$
\begin{gather}
	\text{Assume } n > 1 \land Atomic(n) \\
	\text{Then } n > 1 \text{ and } Atomic(n)
\end{gather}
$$
-  Form: $\forall n \in \mathbb{N}, P(n) \Rightarrow Q(n)$. We could equivalently try to prove $\forall n \in \mathbb{N}, \neg Q(N) \Rightarrow \neg P(n)$ (proof of the contrapositive or indirect proof)
$$
\begin{gather}
	\forall n \in \mathbb{N}, \neg Prime(n) \Rightarrow \neg(n > 1 \land Atomic(n)) \\
	\forall n \in \mathbb{N}, \neg Prime(n) \Rightarrow n \le 1 \lor \neg Atomic(n)
\end{gather}
$$
- $Prime(n): n > 1 \land (\forall d \in \mathbb{N}, d\mid n \Rightarrow d = 1 \lor d = n)$
	- Contrapositive: $\neg Prime(n): n \le 1 \lor \exists d \in \mathbb{N}, d \mid n \land d \neq 1 \land d \neq n$
- $\neg Atomic(n): \exists a, b \in \mathbb{N}, n \nmid a \land n \nmid b \land n \nmid ab$
	- Need to prove a $\exists$ instead of a $\forall$ which can be easier.

### Discuss

$$
\begin{gather}
	\text{Assume } \neg Prime(n) \text{ and } n \le 1 \\
	\text{or there is some } d \neq 1, \neq n \text{ that divides } n \\
	\text{need to find an } a, b \text{ s.t. } n \nmid a, n\nmid b and n \nmid ab \\
	\text{Suppose } n = 6	\text{ (not prime)} \\
	\text{find a, b s.t. } n \nmid a, n\nmid b \text{ and } n \nmid ab\\
	\text{Let } a=3, b=4, n=6
\end{gather}
$$
- **Generalizing**
	- $n \in \mathbb{N}$
	- $\neg Prime(n)$
	- We can find $n_{1}, n_{2}$ s.t. $1 \le n_{1}, n_{2} \le n$ and $n = n_{1} \cdot n_{2}$
	- Then pick $a=n_{1}, b=n_{2}$, we work to prove conclusion

### Proof
$\text{Let }n \in \mathbb{N} \text{ and assume that } n \text{ is not prime}$
$\text{Then we know that either } n \le 1 \text{ or } \exists d \in \mathbb{N}, d\mid n \land d \neq 1 \land d \nmid n$
$\text{Know } n \in \mathbb{N} \text{ and } n \le 1 \text{ or } n > 1$
$$
\begin{align}
	\text{Case 1:} &\text{ Assume } n \le q \\
	&\text{The } n \le 1 \lor \neg Atomic(n) \\
	&\text{is True, as requreid} \\
	\text{Case 2:} &\text{ Assume } n > q \\
	&\text{So } \exists d \in \mathbb{N}, d \mid n \land d \neq 1 \land d \neq n \\
\end{align}
$$
$$
\begin{gather}
	\text{We know } \exists k \in \mathbb{N}, n = d \cdot k \\
	\text{Let } a = d \text{ and } b = k \\
	\text{We need to show } n\nmid a \land n \nmid b \land n \mid ab \\
	\text{so } n \mid ab \\
	\text{Since } n =d \cdot k \text{ with } n, d, k \in \mathbb{N}, \text{ and so } n \nmid a \text{ and } n \nmid b 
\end{gather}
$$
$\text{We have proven that:}$
$$
\begin{gather}
	\forall n \in \mathbb{N}, n > 1 \land Atomic(n) \Rightarrow Prime(n)
\end{gather}
$$
$\text{Next proves:}$
$$
\begin{gather}
	\forall n \in \mathbb{N}, Prime(n) \Rightarrow n > 1 \land Atomic(n)
\end{gather}
$$