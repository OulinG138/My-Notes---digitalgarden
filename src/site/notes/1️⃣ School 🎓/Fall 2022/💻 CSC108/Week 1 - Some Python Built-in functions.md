---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/week-1-some-python-built-in-functions/","dgPassFrontmatter":true}
---

 ```python
 # Built-in Functions
 max(1, 2, 3.5)
3.5
help(round)
Help on built-in function round in module builtins:

round(number, ndigits=None)
    Round a number to a given precision in decimal digits.
    
    The return value is an integer if ndigits is omitted or None.  Otherwise
    the return value has the same type as the number.  ndigits may be negative.

round(1.32423423, 2)
1.32
round(1.235, 2)
1.24
help(abs)
Help on built-in function abs in module builtins:

abs(x, /)
    Return the absolute value of the argument.

abs(-1)
1
round(3.32423)
3
round(1.6)
2
round(2.5)
2



# a*b / 2 in the shell

a = 2
b = 2
area = a*b / 2
area

2.0

```