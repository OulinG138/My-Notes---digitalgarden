---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-148/lecture-notes/week-1-function-design-recipe-recap-2/","dgPassFrontmatter":true}
---


## Quick Recap
1. Examples
2. Header
3. Description
4. Body(For Implementation)
5. Test

&thinsp;

## Testing with purpose

### Doctests: for understanding
```python
def insert_after(lst: list[int], n1: int, n2: int) -> None:
"""After each occurrence of <n1> in <lst>, insert <n2>

>>> lst = [5, 1, 2, 1 ,6]
>>> insert_after(lst, 1, 99)
>>> lst
[5, 1, 99, 2, 1, 99, 6]
"""
```


&thinsp;


### Unit Tests: for assessing "units" of code
- The key technical tools are:
	- the `assertion`
	- the `test_cases`
- e.g. **Pytest**: for automating unit testing
	- name starts with `test_`

```python
def test_simple() -> None:
	input_list = [5, 1, 2, 1, 6]
	insert_after(input_list, 1, 99)
	expected = [5, 1, 99, 2, 1, 99, 6]
	assert input_list == expected # Assertion Statement
```

#### Property-based Testing
- Test examples with library `hypothesis` 
	- We can import and use decorator[^1] from Python Package `hypothesis` which starts with symbol `@` to generate random examples.
	- For Reference: 
		- [Welcome to Hypothesis! — Hypothesis 6.62.0 documentation](https://hypothesis.readthedocs.io/en/latest/)
		- https://www.teach.cs.toronto.edu/~csc148h/winter/notes//testing/hypothesis.html
```python
from hypothesis import example, given, settings
from hypothesis.strategies import text, integers, floats, lists

# 1.Decorator @given defines how the example data is generated.
# generates random examples in respective types
@given(text()) 
@given(integers())
@given(floats())
@given(lists(floats))

# 2.Set "a" as an particular example if it's needed
@example("a") 

# 3.Set a maximum amount of examples to be tested
@settings(max_examples=100)
```

- You can also write import statement in one line:
```python
from hypothesis import given, strategies as st

@given(st.lists(st.integers()))
```




[^1]: A decorator in Python is **a function that takes another function as its argument, and returns yet another function** . Decorators can be extremely useful as they allow the extension of an existing function, without any modification to the original function source code.