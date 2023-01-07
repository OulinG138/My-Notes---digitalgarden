---
{"dg-publish":true,"permalink":"/1-school/winter-2023/csc-148/preview/lecture-01-memory-model/"}
---


```toc
```

&nbsp;

## 去重方法
* 运用Set(集合)去重
```python
lst = list(range(5))
lst.append(4)

lst = list(set(lst))
print(lst)
```

&nbsp;

## is vs. ==
```python
m = [1, 2]
n = [1, 2]

print(f'id(m) = {id(m)}')
print(f'id(n) = {id(n)}')
print(m == n) #值相等
print(m is n) #地址不同
```

&nbsp;

## 二进制
| Number | Binary |
| :-----: |:-----: |
| 1      | 0001   |
| 2      | 0010   |
| 3      | 0011   |
| 4      | 0100   |
| 5      | 0101   |
| 6      | 0110   |
| 7      | 0111   |
| 8      | 1000   |
| 9      | 1001   |
| 10       |   1010     |

```python
# 5 -> 0101

print(bin(5))
```

&nbsp;

## 列表推倒式
* 需求： 需要所有偶数
```python
nums = list(range(1, 11))

# 01
evens = []

for num in nums:
    if num % 2 == 0:
        evens.append(num)

# 02
evens = [num for num in nums if num % 2 == 0]
```

&nbsp;

## 查看Local和Global 
* 使用Debug工具
```python
def mess_about(s, n):
    message = s * n # break point 2: in function call
    s = message
    print(s) # OK * 13
	
if __name__ == '__main__':
    count = 13
    word = 'OK' # break point 1: before function call
    mess_about(count, word)
    print(word) # OK    # break point 3: after function call
```