---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/nov-17-2022-test-module/","dgPassFrontmatter":true}
---


```python
from popQuiz9 import merge_ordered

#From another file
def test_merge_smallest_list1():
	list1 = [1, 2, 3]
	list2 = [0, 3, 14, 20]
	expected[0, 1, 2, 2, 3, 3, 3, 14, 20]

	actual = merge_ordered(list1, list2)
	assert expected == actual

#From the main file
if __name__ == "__main__":
	import pytest
	pytest.main(['popQuizTest.py'])
```