---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/oct-20-2022-read-files/","dgPassFrontmatter":true}
---


# On Week 6 PPT
```python
# read() -> prints the whole txt file in one string

file_name = 'my_file.txt'
file = open(filename, 'r')

file_in_one_string = file.read()

print(file_in_one_string, end='') 

file.close()
```

```python
# for loop in file.txt

file_name = 'my_file.txt'
file = open(filename, 'r')

for line in file:
	print(line, end='')

file.close()
```

```python
# readlines() -> Read the entire file

file_name = 'my_file.txt'
file = open(filename, 'r')

lines_list = file.readlines()
file.close()

for line in lines_list:
	print(line, end='')

#Second Approach

for i in range(len(lines)):
	print(lines_list[i], end='')
```

```python
# while loop
file_name = 'my_file.txt'
file = open(filename, 'r')

line = file.readline()

while line is not '':
	print(line, end='')
	line = file.readline()


file.close()
```


![](https://i.imgur.com/uZjkUv6.png)

