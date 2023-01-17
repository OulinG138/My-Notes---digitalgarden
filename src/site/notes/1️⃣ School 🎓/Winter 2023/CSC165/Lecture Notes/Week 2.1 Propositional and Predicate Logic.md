---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-165/lecture-notes/week-2-1-propositional-and-predicate-logic/","dgPassFrontmatter":true}
---


## Propositional Logic (review from prep)
1. If you push that button, the fire alarm will go off.  $p$ and $q$
	- $p \Rightarrow q$ is an implication. Whenever $p$ is True, it follows that $q$ must be True.
	- $p$: **hypothesis of the implication**
	- $q$: **conclusion of this implication**
- Truth Table
$$
\begin{array}{|c c|c|}
p & q & p \Rightarrow q \\
\hline 
False & False & True \\
False & True & True \\
True & False & False \\
True & True & True
\end{array}
$$
- Vacuous Truth[^1]
$$
\begin{array}{|c c|c |}
p & q & p \Rightarrow q \\
\hline 
False & False & True \\
False & True & True 
\end{array}
$$
- $p \rightarrow q$ and $\neg p \lor q$ are logically equivalent.

&ensp;

2.  If you are a Pens fan , then you are not a Flyus fan.
	-  $p=$  "You are a Pens fan", $q=$  "You are not a Flyus fan."
		- $p \Rightarrow q$ : Suppose you are a Flyus fan. 
			-  $\neg q$ is True.
		- What can we conclude?
			- $p$ must be false or $\neg p$ is True.
			- We can conclude:  $\neg q \Rightarrow \neg p$
3. Terms
	- **Contrapositive**: $p \Rightarrow q$ is logically equivalent to $\neg q \Rightarrow \neg p$ 
	- **Converse** of $p \Rightarrow q$ is $q \Rightarrow p$, they are not logically equivalent.
	- **Biconditional bi-implication**
		- $p \Leftrightarrow q$ says $p$, $q$ denote the same truth value
			- $p$ and $q$ means $(p \Rightarrow q) \land (q \Rightarrow p)$

&ensp;

## Propositions and Predicates
- Consider the propositions:
	- '$2$ is divisible by $3$' is $F$
	- '$3$ is divisible by $3$' is $T$
	- '$4$ is divisible by $3$' is $F$
	- '$5$ is divisible by $3$' is $F$
	- '$4$ is divisible by $3$' is $T$
- Consider Predicate functions:
	- '$x$ is divisible by $3$'
		- $P(x):$ '$x$ is divisible by $3$', where $x \in \mathbb{N}$
			- $P(30)$ is True
			- $P(43) =$ False 
	- $Q(x, y): x^2+y^2=1$, where $x, y \in \mathbb{R}$
	- $R(x): x<x^2-2x+1$, where $x \in \mathbb{N}$ 
		- Is $R(x)$ ever True?
			- $R(0)$ is True
			- $R(10)$ is True
		- Is $R(x)$ always True?
			- No. $R(1)$ is False.

&ensp;

## Express using quantifiers
-   **Existential quantification**: $\exists x \in \mathbb{N}, R(x)$
		- $\exists x \in \mathbb{N} \text{ s.t. } R(x)$ is True
		- $(\exists x \in D, P(x)) \Leftrightarrow (P(x_1) \lor P(x_2) \lor P(x_3) \lor \dots)$
	- **Universal quantification**: $\forall x \in \mathbb{N}, R(x)$
		- $\forall x \in \mathbb{N}, R(x)$ is True
		- $(\forall  x \in D, P(x)) \Leftrightarrow (P(x_1) \land  P(x_2) \land P(x_3) \land \dots)$
	- **Multiple quantifiers**
		- In general, you can reorder variables when both/all universally quantified.
			- Examples:
				- $\forall x \in R$,  $\forall y \in R$,   $x+y=y+x$ 
				-  $\forall y \in R$, $\forall x \in R$, $x+y=y+x$
					- **Multiple universal quantifiers**: We can just package them, $\forall x, y \in R$, $x+y=y+x$
				- <mark style="background: #FF5582A6;">Exception</mark>: $\forall x, y \in \mathbb{R}$, $x-y=y-x$
					- Take $x = 0$ and $y=1$, the statement's false
				- $\exists x \in \mathbb{R}$, $\exists y \in R$, $x-y=y-x$
					- Take $x=0$ and $y=0$
					- **Multiple existential quantifiers**: This is the same as $\exists y \in \mathbb{R}$, $x \in \mathbb{R}$, $x-y=y-x$
	- **Mix of quantifiers**
				-  $\text{Set }A$ = $\{1, 2, 3, 4\}$
					- $\forall x \in A$, $\exists y \in A$, $x+y=5$ is True
					- $\exists y \in A$, $\forall x \in A$, $x+y=5$ is False
			- <mark style="background: #FF5582A6;">Conclusion</mark>: the order of the quantifiers matters when different.



[^1]: A vacuous truth is a conditional or universal statement that is true because the antecedent cannot be satisfied.