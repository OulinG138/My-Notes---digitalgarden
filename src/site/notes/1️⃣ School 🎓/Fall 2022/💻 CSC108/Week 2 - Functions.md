---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/week-2-functions/","dgPassFrontmatter":true}
---


```python
def get_lecture_time(lecture_code: str):
	return 12


def wrap_lecture_time(code: str):
	return get_lecture_time(code)

wrap_lecture_time("CSC108 L0501")
```

```python
def calculate_tax(bill, tax_rate):
	return bill * tax_rate

bill = 87.9

payment = bill + calculate_tax(bill, 0.13)
print(payment)
```