---
{"dg-publish":true,"permalink":"/1-school/winter-2023/csc-148/preview/lecture-07-try-and-exceptions/"}
---

### Example
1. Create my own Exception Error(Optional)
2. Try Module and Except Module
```python
class EvenError(Exception): # -> It's a subclass of Exception
	pass


print('---The start of the Try module---\n')

try: 
	# Error 1
	assert 1 = 2, 'Two numbers are inequivalent' # Assertion Error
	
	# Error 
	x = 6
	if x % 2 == 0:
		raise EvenError("We don't want an even number") # Error that we created.
	
	# Error 3
	1 / 0 # ZeroDivisionError
	
	# No Error
	print('No Error are caught in try module!') # Optional

except AssertionError as ae:
	print(ae)
	print('Caught as AssertionError')

except EvenError as ee:
	print(ee)
	print('Caught as EvenError')

except Exception: 
	print('Caught as Exception')

else:  # Optional
	print('No Errors are found.')

finally: # Optional
	print('This line will always be executed before Try module ends.')

print('\n---The end of the Try module---')
```

