---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/nov-29-2022-class/","dgPassFrontmatter":true}
---


```python
class Dog:
	def __init__(self, name, age, color, size):
		self.name = name
		self.age = age
		self.color = color
		self.size = size

	def run(self):
		print("Hey I\'m {} and I\'m running".format(self.name))

	def sleep(self):
		print("I\'m  sleeping")

	def birthday(self):
		self.age = self.age + 1

	def __eq__(self, other):
		return self.color == other.color and self.size == other.size

	def __str__(self):
		return "I\'m {}. I\'m years old. I am {} and {}".format(self.name, 
        self.age, self.color, self.size)

```
```python
#Console
print(dog1 == dog2)
print(dog1)
```