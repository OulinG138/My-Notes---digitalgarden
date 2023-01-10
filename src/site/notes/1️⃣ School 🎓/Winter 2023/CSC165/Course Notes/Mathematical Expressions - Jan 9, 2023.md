---
{"dg-publish":true,"permalink":"/1-school/winter-2023/csc-165/course-notes/mathematical-expressions-jan-9-2023/"}
---



## Mathematical Preliminaries
1. Description of a Set[^1]
	- Example: First year csc courses
		- $F$:  $\{\text{csc108, csc148, csc165, csc240}\}$
		- $G$: $\{(\text{leafs}, 1), \text{blue}, \{\text{regulation, playoff}\}\}$
2. Size of a Set
	- **Cardinality**[^2]
		- $|F| = 5$
		- $|G| = 3$
		- Empty Set: $|\,\emptyset\,| = 0$
3. Infinite Sets:
	1. Natural Numbers: $\mathbb{N} = \{0, 1, 2, 3, 4, ...\}$
	2. Real Numbers: $\mathbb{R}$
	3. Rational Numbers: $\mathbb{Q}$
	4. Intergers: 
$$
\begin{align}
	\mathbb{Z} &= \{..., -2, -1, 0, 1, 2, ...\}\\
	\mathbb{Z} &= \{0, +1, -1, +2, -2 …\}
\end{align}
$$

&nbsp;

## Finite Strings over 0, 1
1. A finite string over $\{0, 1\}$ is a finite sequence of $b_0b_1b_2 ... b_{k-1}$ where $k$ is positive integer and each of $b_0, b_1, b_2, ...,$ are either $0$ or $1$.
	* Example
		* $10100101$
		* $1$
		* $001$
		* But <mark style="background: #FF5582A6;">NOT</mark> $165$ for example, because its finite number part are digits not binary values.
	* The length of $b_0b_1b_2 ... b_{k-1}$ is $k$.
	* Empty String is typically denoted by the symbol $\,\epsilon\,$ has length $0$.
2.  Another way to describe a Set.
	1. E.g. $\{x \, | \, x \in \mathbb{N} \; and \; 1 \le x < 7\}$
		* $x$: gives a name to element in the set.
		- $|$: such that
		- $x \in \mathbb{N} \; and \; 1 \le x < 7$: conditions on element that must be satisfied if in set.
		- The set of natural numbers that are between $1$ and $6$ inclusive.
	2. E.g. The set of rational numbers: 

$$
\begin{align}
	\mathbb{Q} &= \{\frac{p}{q} \; | \; p, q \in \mathbb{Z} \; and \; q \ne 0\} \\ 
	\mathbb{Q} &= \{\frac{p}{q} \; | \; p \in \mathbb{Z} \; and \; q \in \mathbb{Z}^+\}
\end{align}
$$

3. More abstract examples:
	- set of all valid python programs
	- set of sequences of numbers
	- set of computer networks

&nbsp;


## Operations on Sets
- Consider
	- $X = \{1, 3, 5, 7, 9\}$
	- $Y = \{9, 7, 6, 3, 1\}$
	- $Z = \{1, 9\}$
- **Membership:**

$$
X \in A

\begin{cases}

\text{True}, & \text{where x is an element of A}\\
\text{False},& \text{Otherwise}

\end{cases}
$$

- E.g.
	- $5 \in X \text{ is True}$ 
	- $5 \in Z \text{ is False}$  &#8594; $5 \notin Z \text{ is True}$
- Subset
	* $A \subseteq B$ is True if every element of $A$ is also in $B$ &#8594; A is a subset of B
	* so $Z$ is a subset of $X$, $Z$ is a subset of $Y$
	* $Y$ is a subset of $X$, $X$ is a subset of $Y$
		* **Equality**: $A = B$ is True if $A$ is a subset of $B$ and $B$ is a subset of $A$
		* so $X$ = $Y$
* Other Operations to perform on sets
	* **Union**: $A \cup B$ is the set consisting of all elements that occur in <mark style="background: #FF5582A6;">$A$ or $B$ or in both</mark>
	* **Intersection**:  $A \cap B$ is the set consisting of all elements  that occur in <mark style="background: #FF5582A6;">both $A$ and $B$</mark>
	* **Difference**: $A \setminus B$ is the set consisting of all elements  that occur in <mark style="background: #FF5582A6;">$A$ but not $B$</mark>
	* **Cartesian Product**: $A \times B$ is the set of all pairs of $(a, b)$ where $a \in A$ and $b \in B$
		* e.g. $\{0, 1\} \times \{a, b, c\} = \{(0, a), (0, b), (0, c), (1, a), (1, b), (1, c)\}$
		* Let $A$ and $B$ be non-empty finite sets[^3]. Then the Cartesian Product is finite and it holds: $|A \times B| = |A| \cdot |B|$
	* **Power set**[^4]: $P(A) = \{S \text{ | } S \subseteq A\}$
		* E.g. $A = \{1, 6, 5\}$
			* $P(A) = \{\emptyset, \, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{1, 3\}, \{2, 3\}, \{1, 2, 3\}\}$[^5]



 [^1]: A set is a collection of distinct objects, which we call elements of the set.
[^2]: In mathematics, the cardinality of a set is a measure of the number of elements of the set.
[^3]: Finite sets are sets having a finite/countable number of members.
[^4]: Returns the set consisting of all subsets of A.
[^5]: Every set is a subset of itself, and the empty set is a subset of every set: $A \subseteq A$ and $\emptyset \subseteq A$ are always True.
