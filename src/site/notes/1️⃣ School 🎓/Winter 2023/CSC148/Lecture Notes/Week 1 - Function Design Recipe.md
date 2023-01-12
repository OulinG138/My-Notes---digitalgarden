---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-148/lecture-notes/week-1-function-design-recipe/","dgPassFrontmatter":true}
---


## Quick Recap
1. Examples
2. Header
3. Description
4. Body
5. Test

&nbsp;

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