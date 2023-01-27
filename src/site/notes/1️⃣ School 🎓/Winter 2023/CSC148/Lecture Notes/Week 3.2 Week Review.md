---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-148/lecture-notes/week-3-2-week-review/","dgPassFrontmatter":true}
---


## Memory Model Recap
```python
class Parent:
	def __init__(self, x: int) -> None:
		self.x = x

class Child(Parent):
	def __init__(self, x: int) -> None:
		Parent.__init__(self, x)
		self.y = 10

if __name__ == "__main__":
	c = Child(5)
```

![](https://i.imgur.com/MvQxIZ1.png)

&nbsp;

## isinstance vs. type

```python
if __name__ == "__main__":
	c = Child(5)
	print(isinstance(c, Child), isinstance(c, Parent), type(c)

# Output: True True <class '__main__.Child'>
```