---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/week-3-string-in-memory/","dgPassFrontmatter":true}
---


```python
# When each letter of a variable is all uppercase, meaning we want it to be unchangeable
MIN_AGE = 13
MAX_AGE = 18

def is_teenager (age: int) -> bool:
	return age <= MAX_AGE and age >= MIN_AGE
```


### How does Python Store a string in memory?
![Pasted image 20220929123823.jpg](/img/user/5%EF%B8%8F%E2%83%A3%20Attachments%20%F0%9F%93%84/Pasted%20image%2020220929123823.jpg)
```python
# We can retrieve a specific letter from a string by indexing
>>>str1[0]
“H”
>>>str[1]
“e”
>>>str[5]
Error: string index out of range
```