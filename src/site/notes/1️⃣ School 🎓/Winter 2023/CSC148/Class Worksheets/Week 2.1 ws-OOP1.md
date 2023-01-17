---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-148/class-worksheets/week-2-1-ws-oop-1/","dgPassFrontmatter":true}
---

## Q1
```python
class Spinner:
    """A spinner for a board game."""
    slots: int
    position: int

    def __init__(self, size: int) -> None:
        """Initialize a new spinner with <size> slots.

        A spinner's position always starts at 0.

        Precondition: slots >= 1
        """
        slots = size
        position = 0


if __name__ == '__main__':
    s = Spinner(8)
```

- Memory Model 
![](https://i.imgur.com/zHRpsvg.png)


- Debugging to see the memory model

![](https://i.imgur.com/AHfDAnm.png)

![](https://i.imgur.com/CU6npvT.png)
![](https://i.imgur.com/xv75WqC.png)

![](https://i.imgur.com/BNWBpoP.png)

![](https://i.imgur.com/aLGGywp.png)


&nbsp;

## Q2
- <mark style="background: #FF5582A6;">False Solution</mark>
```python
from datetime import date

class Tweet:
    """A tweet, like in Twitter."""

    def __init__(self, who: str, when: date, what: str) -> None:
        """Initialize a new Tweet."""
        self.userid = who
        self.created_at = when
        self.content = what
        self.likes = 0

	###NOTE: This edit() implementation is incorrect
    def edit(self, new_content: str) -> None:
        """Replace the contents of this tweet with the new message. 
        """
        old_user = self.userid 
        old_date = self.created_at 
        self = Tweet(old_user, old_date, new_content)

if __name__ == '__main__':
	t = Tweet('Anthy', date(2017, 7, 1), 'CANADA!')
	t.edit('150!')
	print(t.content)

# Output: CANADA!
```
- **NOTE**: Re-assigning self doesn’t mutate anything!

&emsp;


- Memory Model
![](https://i.imgur.com/nYJFSjp.png)


- <mark style="background: #BBFABBA6;">Correct Solution</mark>
```python
def edit(self, new_content: str) -> None:
	 self.content = new_content
```