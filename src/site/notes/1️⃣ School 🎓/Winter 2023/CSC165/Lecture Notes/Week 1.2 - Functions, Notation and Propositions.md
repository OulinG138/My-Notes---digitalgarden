---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-165/lecture-notes/week-1-2-functions-notation-and-propositions/","dgPassFrontmatter":true}
---

## Function
- Each element $a \in A$ must map to an element to $b \in B$, but not elements in $b \in B$ be mapped onto.
- The range of $f$ is the set $\{f(x) \text{ | } x \in A\}$
	- $range(f) \subseteq B$
- Example of Functions:
	-  **Predecessor Function**[^1](A unary function)
		- $pred()$: $Z \rightarrow Z$
			- Defined by $pred(x) = x-1$
			- E.g.
				- $pred(7) = 6$
				- $pred(0) = -1$
	- $+: R \times R \rightarrow R$(A binary function)
		- Defined by $+(x, y) = x + y$
	- A function with $k$ arguments: a $k$-ary function

### Predicate
- **Predicate**: A function whose codomain is $(\text{True, False})$
- Examples: 


1. $Z \rightarrow \{\text{True, False}\}$ or $\{\text{T, F}\}$ or $\{1, 0\}$
	- Defined by: 

$$
Even(x) = 

\begin{cases}  

\text{True}, &\text{if x is a multiple of z} \\
\text{False}, &\text{Otherwise} 

\end{cases}
$$

2. $P_{165}: Z \rightarrow \{\text{T, F}\}$
	- Defined by $P_{165}(x): x > 165$
		- e.g. $P_{165}(240)$ is True
	- Given a predicate $P: D \rightarrow \{\text{T, F}\}$
		- We can define $S = \{x \text{ | } x \in D \text{ and } P(x) \text{ is True } \}$


3. Likewise, given a subset $S$ of $D$, we can define a predicate.
	- $P: D \rightarrow \{\text{T, F}\}$
		- Defined by: 


$$
Even(x) = 

\begin{cases}  

\text{T}, &\text{where } x \in S \\
\text{F}, &x \notin S 

\end{cases}
$$
<br/>

## Summation and Product Notation

### Summation
- $1 + 2 + 3 + 4 + … + 100 \rightarrow 1 + 2 + 3 + 4 + i + 100$ 
	- $\sum\limits_{i=1}^{100}{i}$ 
	- $f(i)=i$
- $1 + 3 + 5 + 7 + … + 99 \rightarrow 1 + 2 + 3 + 4 + (2i+ 1)\text{ or }(2i-1) + 100$
	-  $\sum\limits_{i=0}^{49}{(2i+1)}$ or $\sum\limits_{i=1}^{50}{(2i-1)}$
	- $f(i) = 2i + 1$ or $f(i) = 2i - 1$
- $1 + 4 + 7 + 9 + 16 + … + 100 \rightarrow  1 + 4 + 7 + 9 + 16 + i^2+ 100$
	- $\sum\limits_{i=1}^{10}{i^2}$
	- $f(i) = i^2$
- We can use sigma notation to simplify:
	- For integer indices $j \le n$,
	- Defined by $\sum\limits_{i=j}^{n}{f(i)=f(j) + f(j+1) + … f(n-1) + f(n)}$
		- $n$ represents the upper bound and $i=j$ represents the lower bound
	- **Note**: where $j > n$, take  $\sum\limits_{i=j}^{n}{f(i)=0}$
- In Python:
	- When $j > n$  $\rightarrow s = 0$ 
```python
s = 0
for i in range(j, n + 1):
	s += f(i)
```

### Products
- For indices $j \le n$,
	- $\prod_{i=j}^{n}{f(i) = f(j) \times f(j+1) \times … \times f(n-1) \times f(n)}$ 
	- **Note**: where $j > n$, take $\prod_{i=j}^{n}{f(i) = 1}$

&nbsp;


## Propositional Logic
- **Proposition**: A statement that is either True or False.
- Examples:
	- True Statement
		-  $2 + 4 = 6$
	- False Statement
		- $3 - 5 > 0$
	- For every natural number $n$, $n^2 + n + 41$ is prime
		- False: Consider $n = 41$

$$
\begin{align}

&n^2 + n + 41\\
&=41^{2} + 41 +41\\
&=41(41+1+1) \\
&=41 \times 43 \\
&=n^{2}+n+41 \\
\\
\therefore \; &n^2 + n + 41 \text{ is not prime}

\end{align}
$$


```ad-faq
title: Think About

Proposition: Every even integer greater than $2$ is the sum of two prime numbers.
```



[^1]: The predecessor function is a function that maps a natural number n to the previous natural number, n – 1.
	$$pred(n)=\begin{cases}0, &n=0 \\n-1, &n>0\end{cases}$$