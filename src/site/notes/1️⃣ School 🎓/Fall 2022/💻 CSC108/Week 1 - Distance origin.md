---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/week-1-distance-origin/","dgPassFrontmatter":true}
---


# The distance to the origin
```python
def calculate_distance_origin(x: float, 
					y: float) -> float:
	"""Return the distance between the 
	point (x,y) and the origin (0,0).

	>>> calculate_distance_from_origin(3.0, 4.0)
	5.0
	
	>>> calculate_distance_origin(0.0, 0.0)
	0.0
	"""
	return pow(pow(x, 2) + pow(y, 2), 0.5)
```