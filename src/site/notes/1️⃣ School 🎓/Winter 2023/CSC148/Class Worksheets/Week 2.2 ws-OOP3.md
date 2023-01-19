---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-148/class-worksheets/week-2-2-ws-oop-3/","dgPassFrontmatter":true}
---

1. Write code that creates a tweet called misbehaved that is in some way nonsensical. There are at least two ways to do this.
```python
if __name__ = '__main__':
	misbehaved = Tweet('', date(3000, 2, 12), 'A very long tweet' * 1000)
	misbehaved.like(-100)
```

2. Describe a property (something that should be true) that your misbehaved instance has violated.


3. Modify the Tweet class above to prevent your methods from violating this property.