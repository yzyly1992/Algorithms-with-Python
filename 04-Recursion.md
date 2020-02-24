### 04- Recursion

Examples of Recursion: factorial fnction, English ruler, Binary search, file system

4.1 Illustrative Examples
4.1.1 The Tactorial Function
```
def factorial(n):
	if n==0:
		return 1
	else: 
		return n * factorial(n-1)
```
4.1.2 Drawing an English Ruler
4.1.3 Binary Search
Sequential Search: unsorted data
Binary Search: sorted/Indexable data
```
def binary_serach(data, targe, low, high):

	if low > high:
		return False
	else:
		mid = (low + high) // 2
		if target == data[mid]:
			return True
		elif target < data[mid]:
			return binary_search(data, target, low, mid - 1)
		else: 
			return binary_search(data, target, mid + 1, high)
```

Python's os module: os.path.getsize; os.path.isdir; os.path.join(path, filename)

```
import os

def disk_usage(path):
	total = os.path.getsize(path)
	if os.path.isdir(path):
		for filename in os.listdir(path):
			childpath = os.path.join(path, filename)
			total += disk_usage(childpath)

	print('{0:<7}'.format(total), path)
	return total
```

4.2 Analyzing Recursive Algorithms
4.3 Recursion Run Amok
4.3.1 Maximum Recursive Depth in Python
4.4 Further Examples of Recursion
Linear recursion: if a recursive call starts at most one other
Binary recursion: if a recursive call may start tow others
Multiple recursion: if a recursive call may start three or more others

```
## Method 1
def power(x, n):
	if n == 0:
		return 1
	else: 
		return x * power(x, n-1)
```

```
## Method 2
def power(x, n):
	if n == 0:
		return 1
	else:
		partial = power(x, n//2)
		result = partial * partial
		if n % 2 == 1:
			result *= x
		return result
```

4.4.2 Binary Recursion
```
def binary_sum(S, start, stop):
	if start >= stop:
		return 0
	elif start == stop -1:
		return S[start]
	else:
		mid = (start + stop) // 2
		return binary_sum(S, start, mid) + binary_sum(S, mid, stop)
```

4.4.3 Multiple Recursion
```
???
```

4.5 Designing Recursive Algorithms
4.6 Eliminating Tail Recursion

```
def binary_search_iterative(data, target):
	low = 0
	high = len(data)-1
	while low <= high:
		mid = (low + high) //2
		if target == data[mid]:
			return True
		elif target < data[mid]:
			high = mid -1
		else:
			low = mid + 1
return False
```

```
def reverse_iterative(S):
	start, stop = 0, len(S)
	while start < stop - 1:
		S[start], S[stop-1] = S[stop -1], S[start]
		start, stop = start + 1, stop - 1

```

	
4.7 Exercises
R-4.1 
def maxium(S, n):
	max = 0
	while n > 0:
		if S[0] > max:
			max = S[0]
		n = n - 1
		S[0].pop()
	return max

or:

def maxium(S, n):
	if n = 1:
		return S[0]
	if S[0] > S[1]:
		S[1].pop()
	else:
		S[0].pop()
	n = n - 1
	return maxium(S, n)



		
	