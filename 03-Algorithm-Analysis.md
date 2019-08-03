## Algorithm Analysis
Data structure is a systematic way of organizing and accessing data
ALgorithm is a step-by-step  procedure for performing some task in a finite amoun of time
Analysis tool: the running times of algorithms and data structure operations, and space usage.

3.1 Experimental Studies
Measure by time:
```
from time import time
start_time = time()
run alrotithm
end_time()
elapsed = end_time - start_time
```

Counting Primitive Operations
Primitive operations: 
	- Assigning an identifier to an object
	- Determining the object associated with an identifier
	- Performing an arithmetic operation
	- Comparing two numbers
	- Accessing a single element of a Python list by index
	- Calling a function
	- Returning from a function

Measuring Operations as a Function of Input Size
Focusing on the Worst-Cast Input

3.2 The Seven Functions Used in This Book
The Constant Function: f(n) = c
The Logarithm Function: f(n) = logbn
The Linear Function: f(n) = n
The N-Log-N Function: f(n)=nlogn
The Quadratic Function: f(n)= n2
The Cubic Function and Other Polynomials
Summations
The Exponential Function: f(n) = bn
Geometric Sums
3.2.1 Comparing Growth Rates
constant < logarithm < linear < n-log-n < quadratic < cubic < exponential
1 < logn < n < nlogn < n2 < n3 < an
The ceiling and floor functions

3.3 Asymptotic Analysis
3.3.1 The "Big-Oh" Notation: Less than or equal to
Big-Omega: greater than equal to
Big-Theta: grow at the same rate
3.3.2 Comparative Analysis
3.3.3 Example of Algorithm Analysis

3.4 Simple Justification Techniques
3.4.1 By Example
3.4.2 The "Contra" Attack: Contrapositive & Contradiction
3.4.3 Induction and Loop Invariants

