## Python Primer
	1.1 Python Overview
	1.2 Objects in Python
	1.3 Expressions, Operators, and Precedence
	1.4 Control Flow
	1.5 Functions
	1.6 Simple Input and Output
	1.7 Exception Handling
	1.8 Iterators and Generators
	1.9 Additional Python Conveniences
	1.10 Scopes and Namespaces
	1.11 Modules and the Import Statement
	1.12 Exercises

1.1 Python Overview
Intro: High-level computer language; Guido van Rossum 1990s; Python 2 by 2000; Python 3 by 2008;

1.1.1 The Python Interpreter
Intro: Interpreted language; Python interpreter; source code or script; .py suffix; IDEs Integrated Development Environments; 

1.1.2 Preview of a Python Program

1.2 Objects in Python
Intro: Object-Oriented Language and Classes; Case-Sensitive; Reserved Words;

1.2.1 Objects in Python
1.2.2 Creating and Using Objects
Instantiation: the process of creating a new instance of a class; 
Calling Methods: functions
1.2.3 Python's Built-In Classes
Intro: a class is immutable; bool, int, float, list, tuple, str, set, frozenset, dict;

1.3 Expressions, Operators, and Precedence
Logical Operators: boolean vallues - not, and, or
Equality Operators: is, is not, ==, !=
Comparison Operators: <, <=, >, >=
Arithmetic Operators: +, -, *, /, //, %
Bitwise Operators: ~, &, | ^, <<, >>
Sequence Operators: s[j], s[start:stop], s[start:stop:step], s + t, k * s, val in s, val not in s
Operators for Sets and Dictionaries: key in s, key not in s, s1 == s2, s1 != s2, s1<=s2, ... , s1 | s2, s1 & s2, s1 - s2, s1 ^ s2, d[key], d[key] = value, del d[key], key in d, key not in d, d1 == d2, d1 != d2
Extended Assignment Operators: ...

1.4 Control Flow
Intro: Conditional Statements and loops; indented block
1.4.1 Conditionals: if, elif, else
1.4.2 Loops: while, for... in...

1.5 Functions
Intro: functions and methods; def functions(): ...; a return statement is used within the body of a function to indicate that the function should immediately cease execution, and that an expressed value should be returned to the caller. If a return statement is excuted without an explicit argument, the None value is automatically returned. None will be returned if the flow of control ever reaches the end of a function body without having executed a return statement.
1.5.1 Information Passing
Intro: formal parameters; actural parameters; assignment statement; mutable parameters; Default Parameter Values; Keyword Paramenters; 
1.5.2 Python's Built-In Functions
Calling Syntax: abx(x); all(iterable); any(iterable); chr(integer); divmod(x, y); hash(obj); id(obj); input(prompt); isinstance(obj, cls); iter(iterable); len(iterable); map(f, iter1, iter2, ...); max(iterable); max(a,b,c, ...); min(iterable); min(a,b,c,...); next(iterator); open(filename, mode); ord(char); pow(x,y); pow(x,y,z); print(obj1, obj2, ...); range(stop); range(start, stop); range(start, stop, step); revered(sequence); round(x); round(x, k); sorted(iterable); sum(iterable); type(obj);

1.6 Simple Input and Output
1.6.1 Console Input and Output
1.6.2 Files
Calling Syntax: fp = open('sample.txt', wb/rb/a/w); fp.read(); fp.read(k); fp.readline(); fp.readlines(); for line in fp:; fp.seek(k); fp.tell(); fp.write(string); fp.writelines(seq); print(..., file = fp)

1.7 Exception Handling
Intro: Exceptions are unexpected events that occur during the execution of a program. Also known as error or an unanticipated situation.
Common Exception Types: Exception; AttributeError; EOFError; IOError; IndexError; KeyError; KeyboardInterrupt; NameError; StopIteration; TypeError; ValueError; ZeroDivisionError
1.7.1 Raising an Exception
```
def sqrt(x):
	if not isinstance(x, (int, float)):
		raise TypeError('x must be numeric')
	elif x < 0:
		raise ValueError('x cannot be negative')
		#do the real work here ...
```

1.7.2 Catching an Exception
Try-Except Control Structure:
```
try:
	ratio = x/y
except ZeroDivisionError:
	... do someting else ...
```

```
try:
	fp = open('sample.txt')
except IOError as e:
	print('Unable to open the file:', e)
	# e denotes the instance of the exception that was thrown, and printing it causes a detailed error message to be displayed
```
```
except(ValueError, EOFError):
	pass
```

1.8 Iterators and Generators
Intro: An iterator is an object that manages an interation through a seriers of values; An interable is an object, obj, that produces an iterator via the syntax iter(obj).
An instance of a list is an  iterable, but not itself an iterator. With data = [1,2,4,6], it is not legal to call next(data). However, an iterator object can be produced with syntax, i = iter(data), and then each subsequent call to next(i) will return an element of that list.
Lazy Evaluation: for j in range(10000000):

Generators: a `yield` statement is executed to indicate each element of the series. 
```
## Fibonacci numbers
def fibonacci():
	a = 0
	b = 1
	while True:
		yield a
		future = a + b
		a = b
		b = future
```

1.9 Additional Python Conveniences
1.9.1 Conditional Expressions
expr1 if condition else expr2
```
param = n if n >= 0 else -n
result = foo(param)
```
1.9.2 Comprehension Syntax
List comprehension: [ expression for value in iterable if condition ]
```
squares = [k*k for k in range(1, n+1)]
factors = [k*k for k in range(1, n+1) if n % k == 0]
```
list comprehension: [ k*k for k in range(1, n + 1)]
set comprehension: { k*k for k in range(1, n+1)]
generator comprehension: (k*k for k in range(1, n+1))
dictionary comprehension: {k: k*k for k in range(1, n+1)}

1.9.3 Packing and Unpacking of Sequences
Automatic Packing: the assignment data = 2, 4, 6, 8 results in identifier, data, being assigned to the tuple(2, 4, 6, 8)
Unpack a sequenct: a, b, c, d = range(7, 11)
for x, y in [(7,2), (5, 8), (6, 4)]:
Simultaneous Assignments: x, y, z = 6, 2, 5

1.10 Scopes and Namespaces
Scopes: global & local
A namespace manages all identifiers that are currently defined in a given scope.
First-Class Objects: are instances of a type that can be assigned to an identifier, passed as a parameter, or returned by a function.

1.11 Modules and the Import Statement
``` from math import pi, sqrt ```
1.11.1 Existing Modules
Module Name: array, collections, copy, heapq, math, os, random, re, sys, time
Pseudo-Random Number Generation
Formula: next = (a*current + b) % n;
seed(hashtable) -- Initialize the pseudo-random number generator based upon the hash value of the parameter
random() -- returns a pseudo-random floating-point value in the interval[0.0, 1.0).
randint(a,b) -- returns a pseudo-random integer in the closed interval[a,b]
randrange(start, stop, step) -- ...
choice(seq) -- returns an element of the given sequence chosen pseudo-randomly
shuffle(seq) -- reorders the elements of the given sequence pseudo-randomly

1.12 Exercises

R-1.1
```
def is_multiple(n, m):
	if n>=m && n % m == 0:
		return True
	else:
		return False
```

R-1.2
```
def is_even(k):
	return (k & 1 == 0)
```

R-1.3
```
def minmax(data):
	min=max=data[0]
	for i in data:
		if min >= i:
			min = i
		if max <= i:
			max = i
	return min, max
```
R-1.4
```
def sMulti(l):
	sum = 0
	for i in range(1, l+1):
		sum += i*i
	return sum
```	

R-1.5
```
total = sum(i*i for i in range(1, n+1))
```

R-1.6
```
total = sum(i*i for i in range(1, n+1) if i%2 != 0)
```

R-1.8: n+k

R-1.9: range(50, 81, 10)

R-1.10: range(8, -10, -2)

R-1.11: [pow(2,i) for i in range(9)] or [2**i for i in range(9)]

R-1.12
```
def ownChoice(data):
	return data[randrange(len(data))]
```

R-1.13
```
def reverse(data):
	return [data[-i-1] for i in range(len(data))]
```

R-1.14
```
def has_odd_pair(data):
	count = 0
	for j in range(len(data)):
		if data[j] % 2 == 1:
			count++
			if count == 2:
				return True
		return False
```

R-1.15
```
def disNum(data):
	countedList = []
	for i in data:
		if i in countedList:
			return False
		else:
			countedList.append(i)
	return True
```

R-1.16
```
data[j] = data[j] * factor
```

R-1.17
```
def scale(data, factor):
	for i in range(len(data)):
		data[i] = data[i] * factor
	return data
```

R-1.18
```
[ k*(k+1) for k in range(10) ]
```

R-1.19
```
[chr(k) for k in range(97, 123)]
```

R-1.20
```
def shuffle(data):
	newdata = []
	while data is not []:
		newdata.append(data.pop(randint(0, len(data))
	return newdata
```

R-1.21
```
lines = []
while True:
	try:
		single = input()
		lines.append(single)
	except EOFError:
		break

print('\n'.join(reversed(lines)))
```


