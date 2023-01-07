---
{"dg-publish":true,"permalink":"/1-school/fall-2022/csc-108/nov-15-2022-main/"}
---


```python
# This is file1
def func(x):
	return x + 1

print(__name__)

if __name__ == '__main__':
	#This code does not get executed when this file1 is imported.
	print(func(5))
```

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


## Test Module
```python
#We don't want to run this part of code when the files is imported.
if __name__ == '__main__':
	import doctest
	doctest.testmod(f'filename', #filename)
```