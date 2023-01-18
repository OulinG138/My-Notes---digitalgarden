---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-165/lecture-notes/week-2-2-mixed-quantifiers-negationand-expressing-mathematical-statements/","dgPassFrontmatter":true}
---


## Negation
- $\forall \in D, P(x)$ says every $x$ in $D$ is such that $P(x)$ is True
	- **Negation**: $\neg (\forall \in D, P(x))$  says not  every $x$ is such that $P(x)$ is True
		- i.e. 
			- some $x \in D$ is such that $P(x)$ is false
			-  some $x \in D$ is such that $\neg P(x)$ 
			- $\neg (\forall \in D, P(x)) \Leftrightarrow \exists x \in D, \neg P(x)$
- $\exists x \in D, P(x)$ says some $x \in D$is such that $P(x)$ is True
	- **Negation**: $\neg (\exists \in D, P(x))$ says no $x \in D$ is such that $P(x)$ is True
		- i.e.
			- Every $x \in D$ is such that $P(x)$ is True
			- Every $x \in D$ is such that $\neg P(x)$ 
			- $\neg (\exists \in D, P(x)) \Leftrightarrow \forall x \in D, \neg P(x)$


### Example
- Suppose: 
	- Domain $E:$ $\text{Set of Employee}$
	-  Predicate
		-  $O(x):$ "employee $x$ earns over $50,000$,  where $x \in E$"
		- $F(x):$ "employee $x$ is female, where $x \in E$"
```ad-faq
title: Write following sentence in symbolic form.

<br/>

<center><font color="#87CEEB">All employee earning over 50,000 are female</font color></center>

- <mark style="background: #FF5582A6;">False solutions</mark>:
	- $\forall x \in E, O(x) \land F(x):$ says all employee who earn over 50,000 and are female
	- $\forall x \in E, F(x) \Rightarrow O(x):$ says all female employee earn over 50,000
- <mark style="background: #ADCCFFA6;">Correct solution</mark>: $\forall x \in E, O(x) \Rightarrow F(x)$
- **Negation**:
	- Not all employee earn over 50,000 are female *(In English)*
	- $\neg (\forall x \in E, O(x) \Rightarrow F(x))$
		- Simplified: $\exists x \in E, \neg(O(x) \Rightarrow F(x))$
```


&nbsp;

## De Morgan's Rules
- $\neg (p \lor q) \equiv \neg p \land \neg q$
- $\neg (p \land q) \equiv \neg p \lor \neg q$
- $p \Rightarrow q \equiv \neg p \lor q$
- $\neg (p \Rightarrow q) \equiv \neg (\neg p \lor q) \equiv p \land \neg q$
- $\neg (\forall x \in E, O(x) \Rightarrow F(x)) \equiv \exists x \in E, O(x) \land \neg F(x)$

&nbsp;

## Precedence Rule
- $P(x) \lor Q(x) \Leftrightarrow R(x)$ is 
- Precedence Hierarchy (from highest to lowest):
	1. $\neg$
	2. $\lor, \land,$ 
	3. $\Leftrightarrow, \Rightarrow$
	4. $\forall, \exists$
- Example:
	- $P(x) \lor Q(x) \Rightarrow R(x)$ is the same as $(P(x) \lor Q(x)) \Rightarrow R(x)$


&nbsp;


## Divisibility
- **Definition**: Let $n, d \in \mathbb{Z}$. We say that $d$ divides $n$ or $n$ is divisible by $d$ if and only if there exists a multiplier $k \in \mathbb{Z}$ such that $n = d\cdot k$.
- **Notation**: $d \mid k$, represents '$d$ divides $n$'
	- $\mid$ is a predicate like $=, <, >$
- Examples:
	- $3 \mid 6$ True
	- $3 \mid 7$ False

```ad-faq
title: If an integer divides 10 then it divides 100.

- $\forall n \in \mathbb{Z}, n \text{ divides } 10 \Rightarrow n \text{ divides } 100$
- $\forall n \in \mathbb{Z}, (\exists k \in \mathbb{Z}, 10=k \cdot n) \Rightarrow (\exists m \in \mathbb{Z}, 100 = m \cdot n)$
- $\forall n \in \mathbb{Z}, n \mid 10 \Rightarrow n \mid 100$
```
