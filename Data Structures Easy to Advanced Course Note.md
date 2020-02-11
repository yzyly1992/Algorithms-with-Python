## Big-O Notation

Big-O Notation: gives an upper bound of the complexity in the **worst** case, helping to quatify performance as the input size becomes **arbitrarily large**.
Constant Time: O(1)
Logarithmic Time: O(log(n))
Linear Time: O(n)
Linearithmic Time: O(nlog(n))
Quadric Time: O(n2)
Cubic Time: O(n3)
Exponential Time: O(bn), b > 1
Factorial Time: O(n!)

O(n + c) = O(n)
O(cn) = O(n), c > 0

f(n) = 7log(n)3 + 15n2 + 2n3 + 8
O(f(n)) = n3

Finding all subsets of a set - O(2n)
Finding all permutations of a string - O(n!)
Sorting using mergesort - O(nlog(n))
Iterating over all the cells in a matrix of size n by m  - O(nm)

## Static and Dynamic Arrays

A static array is a fixed length container containing n elelments indexable from them range [0, n-1].

Use
1) Storing and accessing sequential data
2) Temporarily storing objcets
3) Used by IO routines as buffers
4) Lookup tables and inverse lookup tables
5) Can be used to return multiple values from a function
6) Used in dynamic programming to cache answers to subproblem

Complexity
Access O(1)
Search O(n)
Insertion N/A O(n)
Appending N/A O(1)
Deletion N/A O(n) ## Shift over, rerange all

Dynamic Array can grow and shrink in size.

## Singly and Doubly Linked Lists

A linked list is a sequential list of nodes that hold data which point to other nodes also containing data.

Use
1) Used in many List, Queue & Stack implementations.
2) Great for creating circular lists.
3) Can easily model real world objects such as trains.
4) Used in separate chaining, which is present certain Hashtable implementations to deal with hashing collisions.
5) Often used in the implementation of adjacency lists for graphs.

Term
Head: The first node
Tail: The last node
Pointer: Reference to another node
Node: An object containing data and pointers

Singly linked lists only hold a reference to the next node.
With a doubly linked list each node holds a reference to the next and prevous node.

Singly Linked: Pros Use less memory, simpler implementation
Cons: Cannot easily access previous elements
Doubly Linked: Pros: Can be traversed backwards
Cons: Takes 2x memory

    Sinly   Doubly
Search O(n) O(n)
Insert at head O(1) O(1)
Insert at tail O(1) O(1)
Remove at hear ...
Remove at tail O(n) O(1)

 
