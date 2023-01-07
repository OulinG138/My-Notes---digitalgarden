---
{"dg-publish":true,"permalink":"/1-school/winter-2023/csc-148/preview/lecture-04-ad-ts/"}
---

# 栈和队列

```toc
```

&nbsp;


## Stack 后进先出
```python
class Stack:
    def __init__(self):
        self.items = []
        #self.items: list[int] = list()

    def push(self, item) -> None:
        self.items.append(item)

    def pop(self):
        return self.items.pop() if not self.is_empty() else None

    def peek(self):
        return self.items[-1] if not self.is_empty() else None

    def is_empty(self):
        return self.items == []

    def size(self):
        return len(self.items)

    def __contains__(self, item):
        return item in self.items
```

&nbsp;

### Leetcode Q20

> Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', 
determine if the input string is valid.
>
>An input string is valid if:
> 1. Open brackets must be closed by the same type of brackets.
> 2. Open brackets must be closed in the correct order.
> 3. Every close bracket has a corresponding open bracket of the same type.
> 
> E.g. '([{}])'

```python
class Solution:
    def isValid(self, s: str) -> bool:
        stack = Stack()
        for ch in s:
            if ch == '(':
                stack.push(')')
            elif ch == '{':
                stack.push('}')
            elif ch == '[':
                stack.push(']')
            elif stack.is_empty() or ch != stack.pop():
                return False
        return stack.is_empty()


if __name__ == '__main__':
    s = Solution()
    s.isValid("([{}])")
    s.isValid("([)]")
```

&nbsp;

## Queue 先进先出
```python
class Queue(object):
    def __init__(self):
        self.items = []
    
    def is_empty(self):
        return self.items == []
    
    def enqueue(self, item) -> None:
        self.items.append(item) 
	
    def dequeue(self):
        return self.items.pop(0) if not self.is_empty() else None

    def front(self):
        return self.items[0] if not self.is_empty() else None
    
    def __len__(self):
        return len(self.items)

    def __contains__(self, item):
        return item in self.items
```

&nbsp;

### 内置队列
```python
from queue import Queue

class Queue(object):
	def __init__(self):
		self.items = []

if __name__ == "__main__":
	q = Queue()
	q.get() # dequeue()
	q.put() # enqueue() 
	q.empty()
```


&nbsp;

## Leetcode Q232 - 用栈实现队列
```python
class MyQueue(object):

    def __init__(self):
        self.input = []
        self.output = []

    def push(self, x):
        self.input.append(x)
    
    def pop(self):
        self.peek()
        return self.output.pop() if self.empty() else None
    
    def peek(self):
        if not self.output:
            while self.input != []:
                self.output.append(self.input.pop())
        return self.output[-1] if self.empty() else None

    def empty(self):
        return self.input == [] and self.output == []
```


&nbsp;

## Leetcode Q225 - 用队列实现栈
```python
class MyQueue(object):

    def __init__(self):
       self.queue = []

    def push(self, x) -> None:
        self.queue.append(x)
        for _ in range(len(self.queue) - 1):
            self.queue.append(self.queue.pop(0))
    
    def pop(self):
        return self.queue.pop(0)
    
    def peek(self):
        return self.output[0] if self.empty() else None

    def empty(self):
        return self.input == [] and self.output == []
```