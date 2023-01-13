---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-148/preps/prep-2/","dgPassFrontmatter":true}
---

## Example from the reading material
- Link: [2.1 Introduction to Object-Oriented Programming (toronto.edu)](https://www.teach.cs.toronto.edu/~csc148h/winter/notes/object-oriented-programming/oop_intro.html)

```python
class Tweet:
    # previous content omitted for brevity

    def __init__(self, who: str, when: str, what: str) -> None:
        """Initialize a new Tweet.
        """
        self.userid = who
        self.created_at = when
        self.content = what
        self.likes = 0

if __name__ == '__main__':
    t1 = Tweet('Giovanna', "2017, 9, 18", 'Hello')
    print(t1.userid)
```

- Diagrams
![](https://i.imgur.com/A6BtKgS.png)
![](https://i.imgur.com/iLX8H57.png)


- Explain the process by debugging
1. 
![](https://i.imgur.com/W35eGaf.png)


2. 
![](https://i.imgur.com/JiL8mHG.png)

3. 
![](https://i.imgur.com/iYFoxTw.png)

4. 
![](https://i.imgur.com/yodO34q.png)

5. 
![](https://i.imgur.com/06R5lM1.png)


## From the weekly quiz
- When calling a method in a class, you can either call it with the created instance/object `team` or directly with the class name `HockeyTeam`.
![](https://i.imgur.com/ASy8a0C.png)


