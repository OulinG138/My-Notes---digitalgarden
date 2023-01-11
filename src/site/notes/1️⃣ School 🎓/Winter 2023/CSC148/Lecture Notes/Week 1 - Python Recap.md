---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-148/lecture-notes/week-1-python-recap/","dgPassFrontmatter":true}
---


## Tracing Simple Code
1. 
```python
x = [1, 2, 3]
y = x
y = y + [4]
print(x, y)

# Output: [1, 2, 3] [1, 2, 3, 4]
```

![](https://i.imgur.com/BPA4Swb.png)


2. 
```python
L = [[1, 2], [3, 4], [5, 6]]
for item in L:
	 item[1] = 88
print(L)

# Output: [[1, 88], [3, 88], [5, 88]]
```

![](https://i.imgur.com/Td0tVxA.png)


3. For Loop Gotcha
```python
lst = [6, 2, 0, 44]
for item in lst:
	 item = item + 1
print(lst)

# Output: [6, 2, 0, 44]
```

![](https://i.imgur.com/bHFQIhu.png)



&nbsp;


## Function
- Terminology
	- **Frame**: Data about a function call (including local variables)
	- **Call Stack**: A collection of the frames of the functions that are currently running.
- Example: 
```python
def mess_about(s, n):
    message = s * n 
    s = message
	
if __name__ == '__main__':
    count = 13
    word = 'OK' 
    mess_about(count, word)
```

[[1️⃣ School 🎓/Fall 2022/💻 CSC108/Week 8 -  '__main__' block\|Week 8 -  '__main__' block]]

- Step 1
![](https://i.imgur.com/WzVkH8g.png)
![](https://i.imgur.com/5UVZa4J.png)

- Step 2
![](https://i.imgur.com/ExXg2r7.png)
![](https://i.imgur.com/LUUd5dw.png)


- Step 3
![](https://i.imgur.com/A2kzHbN.png)
![](https://i.imgur.com/dARonFp.png)

- Step 4
![](https://i.imgur.com/9gxkWpS.png)
![](https://i.imgur.com/9bUeG1D.png)



- Step 5: Outside of `mess_about` function
![](https://i.imgur.com/jRQTL4M.png)

