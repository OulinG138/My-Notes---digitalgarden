---
{"dg-publish":true,"permalink":"/1-school/winter-2023/csc-148/preview/lecture-02-oop/"}
---



# 类
* Classes are description of types of things(a template, like DNA). Objects are specific instances of a type(like clones).
* We usually want to **encapsulate** our code, so that people using our classes don't need to know how they are implemented.

```toc
```

&nbsp;

## 类的组成
1. 类的名称
2. 类的属性
3. 类的方法


## 类属性 vs. 实例属性
```python
class Cat(object):

    z = 'z' # 类属性
            # 在__init__之前

    def __init__(self, x, y):
        self.x = x # 实例属性

    def __len__(self):
        return 3
    
    def __repr__(self):
        pass
```


## lambda方法
```python
# 01
def add(a: int, b: int) -> int:
    return a * b

# 02
add = lambda a, b: a * b
```


### 更多应用
```python
nums = [1, 2, 3, 4, 5]

lst1 = list(map(lambda x: x ** 2, nums)) # map(func, *iterables) 计算
list(filter(lambda x: x % 2 == 0, nums)) # filter(func, *iterables) 取出
print(lst1)
```


&nbsp;

## Arguments
### Arbitrary Arguments 任意长度参数
```python
def say_hi(*kids):
    print("hi, ", end = ' ')
    for name in names:
        print(name, end = ' ')
    print()

if __name__ == '__main__':
	names = ['Kevin', 'Anthony', 'James']
	say_hi(names)
```


### Keyword Arguments
```python
def show_info(name, age):
    print(f'My name and is {name} and age is {age}.')

if __name__ == '__main__':
	show_info('Anthony', 19)
```




