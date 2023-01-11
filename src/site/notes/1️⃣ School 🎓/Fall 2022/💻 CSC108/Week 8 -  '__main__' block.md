---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/week-8-main-block/","dgPassFrontmatter":true}
---


## What does it do?
- We can use an  `if __name__ == '__main__'`  block to allow or prevent parts of code from being run when the modules are imported.
```python
# This is file1
def func(x):
	return x + 1

print(__name__)

if __name__ == '__main__':
	#This code does not get executed when this file1 is imported.
	print(func(5))
```


&nbsp;

## Choosing Text Cases
* Size
	* No items or empty
	* Only one item
	* Several items
	* Some interesting cases
* Dichotomies
		* Either/Or Situations
		* even/odd
		* vowel/non-vowel
		* postive/negative
		* etc.
* Boundaries
	* threshold
		* <>=
* Order
	* Differences in the input's order


&nbsp;

## Test Module
```python
# We don't want to run this part of code when the files is imported.
if __name__ == '__main__':
	import doctest
	doctest.testmod(f'filename', #filename)
```