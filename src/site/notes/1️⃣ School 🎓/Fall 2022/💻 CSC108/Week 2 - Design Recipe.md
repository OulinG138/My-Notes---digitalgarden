---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/week-2-design-recipe/","dgPassFrontmatter":true}
---


```python
#Design Recipe

def format_name(first_name: str, last_name: str) -> str
"""
Return a string with the format last_name, first_name
>>>format_name("Anthony", "Wang")
"Anthony, Wang"

>>>format_name("Janos, Ren")
"Janos, Ren"
"""
return last_name + ", " + first_name


def to_listing(first_name: str, last_name: str, phone_number: str) -> str
"""
Return a string with the format last_name, first_name: phone_number

>>>to_listing("Fernando", "James", "12345")
"James, Fernando: 12345"

>>>to_listing("Anthony", "Wang", "54321")
"Anthony, Wang: 54321"
"""
return format_name(first_name, last_name) + ": " + phone_number
```