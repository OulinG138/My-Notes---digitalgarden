---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/fall-2022/csc-108/week-7-get-team/","dgPassFrontmatter":true}
---


```python
def get_team(athlete_to_sports: dict[str, list[str]], sport: str) -> list[str]:
	"""Return a sorted list of the atheletes from athlete_to_sports who play 
    sport. In athlete_to_sports, each key is an athlete and each value is a 
    list of sports that athlete plays.
    >>> D = ["TF":]
    """

	team = []
	
	#First Approach
	for athlete in athlete_to_sports:
		for sports_played in athlete_to_sports[athlete]:
			if sports_played == sport:
				team.append(athlete)
			
	return team


	#Second Approach
	for athlete in athlete_to_sports::
		if sport in athlete_to_sports[athlete]:
				team.append(athlete)
			
	return team
```