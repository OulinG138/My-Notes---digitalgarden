---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/week-3-sum-evens/","dgPassFrontmatter":true}
---


```python
def sum_evens(nested_list: list) -> list:
"""Return a list with the sum of the even numbers in 
each sublist of nested_list


>>>sum_evens([[2, 4, 7 ,9], [2, 5, 8]])
[6, 10]
>>>sum_evens([[]])
[0]
>>>sum_evens([], [1, 3])
[0, 0]
"""

for i in range(len(nested_list)):
	acc = 0
	for value in nested_list:
		if value % 2 == 0:
			acc = acc + value
		sum_evens_list.append(acc)


return sum_even_list
```

```python
def mins_to_max(nested_list: list[list]) -> None:
"""modify nested_list changing the min in each sublist
to be the max in nested_list.

>>>my_list([[1, 4, 8],[2, 18]])
>>>mins_to_max(my_list)
>>>my_list
[[18, 4, 8],[18, 18]]
"""

max_values = []

for sublist in nest_list:
	max_values.append(max(sublist))

max_value = max(max_values)

for sublist in nested_list
	min_value = min(sublist)
	for i in range(len(sublist)):
		if sublist[i] == min_value:
			sublist[i] = max_value
```