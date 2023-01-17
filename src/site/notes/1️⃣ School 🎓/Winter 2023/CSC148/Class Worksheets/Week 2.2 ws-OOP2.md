---
{"dg-publish":true,"dg-home":false,"permalink":"/1-school/winter-2023/csc-148/class-worksheets/week-2-2-ws-oop-2/","dgPassFrontmatter":true}
---


## Question
- Here is the documentation for our Tweet class:
```python
class Tweet:
"""A tweet, like in Twitter."""

content: str 
userid: str 
created_at: 
date likes: int

	def __init__(self, who: str, when: date, what: str) -> None:
	"""Initialize a new Tweet."""
	
	def like(self, n: int) -> None:
	"""Record the fact that this tweet received <n> likes.
	These likes are in addition to the ones <self> already has. """
	
	def edit(self, new_content: str) -> None:
	"""Replace the contents of this tweet with the new message. """


class User:
"""A Twitter user."""

# Attribute types 
userid: str 
bio: str 
tweets: List[Tweet]
```

&nbsp;

## Solution
- Complete `class User`
```python
from datetime import date

class User:
"""A Twitter user."""

# Attribute types 
userid: str 
bio: str 
tweets: set{Tweet}

	def __init__(self, userid: str, bio: str) -> None:
	"""Initialize a new user with the given id and bio.
		
	The new user initially has no tweets. 
	"""
		self.userid = userid
		self.bio = bio
		self.tweets: set{Tweet} = set()

	def tweet(self, message: str) -> None:
	"""Record that this User made a tweet with the given content.
	
	Use date.today() to get the current date for the newly-created
	tweet. 
	"""
		new_tweet = Tweet(self.userid, date.today(), message)
		self.tweets.append(new_tweet)

	def follows(self, userid: str) -> None:
		"""
		Record the fact that this user follows another with the 
		given userid.

		>>> u = User(“Sophia”, “This is Sophia”)
		>>> u.follows(“Diane”)
		"""
		self.tweets.add(userid)
```