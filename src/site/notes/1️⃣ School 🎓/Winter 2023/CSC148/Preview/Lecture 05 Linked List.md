---
{"dg-publish":true,"permalink":"/1-school/winter-2023/csc-148/preview/lecture-05-linked-list/"}
---

## Components
* Predecessor 前驱节点
* Successor 后继节点
![](https://i.imgur.com/1BYO8bd.png)

```python
from typing import Any, Optional

class Node: # 单一存储的容器被称为Node
items: Any
next: Optional[Node]
```


```python
from typing import Any, Optional

"""A Node class represents a node of the list"""
class Node(object):

	def __init__(self, item: Any):
		self.item = item
		self.next = None # next是一个python关键词

class LinkedList(object):

	def __init__(self, head = None):
		self.head = head

	def print_items(self) -> None:
		"""Print out each item in this linked list."""
		curr = self.head
		while curr is not None:
			print(curr.item)
			curr = curr.next

	def traverse(self) -> list:
		result = list()
		curr = self.head
		while curr is not None:
			result.append(curr.item)
			curr = curr.next
		return result

	def is_empty(self) -> bool:
		return self.head is None

	def __len__(self) -> int:
		"""Return the number of elements in this list

		>>> lst = Linkedlist()
		>>> len(lst) # Equivalent to lst.__len__()
		0
		"""
		if self.is_empty():
			return 0

		node_count = 0
		curr = self.head
		while curr is not None:
			node_count += 1
			curr = curr.next
		return node_count

	def __contains__(self, item):
		if self.is_empty():
			return False

		curr = self.head
		while curr is not None:
			if item == curr.item:
				return True
			curr = curr.next
		return False

	def replace(self, old, new):
		curr = self.head
		while curr is not None:
			if curr.item == old:
				curr.item = new
			curr = curr.next
	
			

	def __getitem__(self, index: int) -> int:
		n = self.__len__()
		#if index < 0: Accepts negative indexes
		#	index += n

		if self.is_empty() or index < 0 or index >= n:
			return None
		# index in [0, n)
		count = 0
		curr = self.head
		while curr is not None:
			if count == index:
				return curr.item
			count += 1
			curr = curr.next

	def append(self, item: Any) -> None:
		"""Append <item> to the ned of thist list.
		
		>>> lst = LinkedList()
		>>> lst.append(1)
		>>> lst.head.item
		1
		>>> lst.append(2)
		>>> lst.head.next.item
		2
		"""
		if is_empty():
			self.head = Node(item)	
			return None # stop and return nothing

		curr = self.head
		while curr.next is not None:
			curr = curr.next
		curr = Node(item)	# rear

	def pop(self, index):
		if index > len(self) - 1:
			raise IndexError

		if index == 0:
			first = self.head
			self.head = first.next
			first.next = None
			return first.item


		count = 0
		curr = self.head
		while curr is not None:
			if count + 1 == index:
				remove_node = curr.next
				curr = remove_node.next
				remove_node = None
				return remove_node.item

			count += 1
			curr = curr.next
			
			


def create_linked_list(nums: list) -> LinkedList:
	head = Node(nums[0])
	lst = LinkedList(head)
	rear = head # rear: pointing at the last node of the linkedlist
	for num in nums[1:]:
		node = Node(num)
		rear.next = node
		rear = rear.next
	return lst

if __name__ == '__main__':
	nums = [1, 2, 3]
	head = create_linked_list(nums)
	#items = head.traverse()
	#print(items)
	#print(len(head))
	head.pop(1)
```