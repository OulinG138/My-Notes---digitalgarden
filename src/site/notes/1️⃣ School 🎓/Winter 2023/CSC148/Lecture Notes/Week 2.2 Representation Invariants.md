---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-148/lecture-notes/week-2-2-representation-invariants/","dgPassFrontmatter":true}
---

## What is Representation Invariants
- **Defintion**: A representation invariant is a property of the instance  
attributes that every instance of a class must satisfy.
- Example:
	- (in words) This tweet’s content is at most 280 characters.
	- (in code) `len(self.content) <= 280`
- Why should we care about representation invariants?
	- Undocumented assumptions/conditions is a huge source of bugs!
- *When given an instance of that class, we can assume that every representation invariants is satisfied.*
![](https://i.imgur.com/xN0pGgz.png)


&nbsp;

## Strategies
1. **Use preconditions**
	- Require client code to call methods with “good” inputs.  Make no promises if it doesn’t. Therefore, the method doesn’t need to check that preconditions are met.
	- ![](https://i.imgur.com/BX5JjR4.png)
2. ignore bad inputs
	- Accept a wide range of inputs. If an input would cause an RI to be violated, do not perform the work of the method. Also known as *failing silently*.
	- ![](https://i.imgur.com/kYVCd1d.png)
3. Fix "bad" inputs
	- Accept a wide range of inputs. If an input would cause an RI to be violated, change the input to a “reasonable” or default value. Then continue with the rest of the method.
	- ![](https://i.imgur.com/5DMlWd2.png)

&nbsp;

## Representation  v.s. Preconditions
![](https://i.imgur.com/t7ZXQ75.png)


