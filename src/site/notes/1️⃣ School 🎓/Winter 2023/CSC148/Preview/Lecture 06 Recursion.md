---
{"dg-publish":true,"permalink":"/1-school/winter-2023/csc-148/preview/lecture-06-recursion/"}
---

```toc
```

## Understand Recursion

###  Factorial 
```python
# for loop
def calc(n: int) -> int:
	result = 1
	for i in range(1, n + 1):
		result *= i
	return result	

if __name__ == '__main__':
	n = 3
	res = calc(n)
	print(f'{n}! = {res}')
```


### Factorial with Recursion
$$
\begin{align}
0! &= 1 \\ 
1! &= 1 
\end{align}
$$
$$
\begin{align}
f(n) &= n! \\
f(n-1) &= (n-1)! \\

f(n) &= n * (n-1)! \\
	 &= n * f(n-1)	
\end{align}
$$

```python
def factorial(n):
	if n == 0: #设为底 trivial case
		return 1
	return n * factorial(n - 1) #Decomposition Step

if __name__ == '__main__':
	n = 3
	res = calc(n)
	print(f'{n}! = {res}')
```

## Recursive Types
* "N-1" approach: handle one entity, then call the recursion N-1 entities
* Divide in 2 or more subproblems: apply recursion for each half, quarter, etc. of the problem
* Other ways...

&nbsp;

## Leetcode Q509 - Fibonacci Number

* Fibonacci Number:
	* $f(0) = 1$
	* $f(1) = 1$
	* $f(n) = f(n-1) + f(n-2)$ when  $x \ge 2$

```python
def f(n: int) -> int:
	if n == 0 or n == 1:
		return 1
	return f(n - 1) + f(n - 2)
	
if __name__ == '__main__':
	for i in range(10):
		print(f'f{i} = {f(i)}')
```

&nbsp;

## Tail Recursion
* Tail Call
```python
def f(x):
	return g(x)

def f(x):
	if x > 0:
		return m(x)
	return n(x)
```

* Not Tail Call
```python
# Case 1
def f(x):
	y = g(x)
	return y

# Case 2
def f(x):
	return g(x) + 1
```

### Tail Recursion vs. Iteration
* Tail Recursion and iteration is the same in terms of time complexity
* It reduces space complexity from the simple recursion.
```python
def factorial(n, pre_res):
	if n == 1:
		return pre_res
	return factorial(n - 1, pre_res * n)

if __name__ == '__main__':
	print(factorial(3, 1))
```


## Problem: Hanoi Problem
