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

## Stack

A stack is a one-ended linear data structure which models a real world stack by having two primary operations, namely push and pop. lifo 

Instructions
pop()
push()

Used
text editor
compiler syntax checking for matching brackets and braces
model a pile of books or plates
used behind the scenes to support recursion by keeping track of previous function calls
depth first search (DFS) on a graph

Example - Brackets
Let S be a stack
For bracket in bracket_string:
    rev = getReversedBracket(bracket)
    if isLeftBracket(bracket):
        S.push(bracket)
    Else If S.isEmpty() or S.pop() != rev:
        return false
return S.isEmpty()

Tower of Hanoi

Stack Source Code

## Queue

A queue is a linear data structure which models real world queues by having two primary operations, namely **enqueue/offer** and **dequeue/pull**. Add element to the back, remove element from the front.

Used

waiting line models
keep track of the x most recently added elements
web server request management where you want first come first serve
breath first search(BFS) graph

Queue Example - BFS

## Priority Queues(PQs) with an interlude on heaps

A priority queue, each element has a certain priority. Priority queues only supports comparable data, meaning the data inserted into the priority queue must be able to be ordered in some way either from least to greatest or greatest to least. 

## Heap

A heap is a tree based DS that satisfies the heap invariant: if A is a parent node of B then A is ordered with repect to B for all nodes A, B in the heap.

Max heap, min heap

Used
Dijkstra's Shortest Path algorithm
dynamically fetch the 'next best' or 'next worst' element.
Huffman coding
Best First Search (BFS) algorithms
Minimum Spanning Tree (MST) algorithms

Binary Heap Construction O(n)

## Turning Min PQ into Max PQ

## Ways of Implementing a PQ

Binary Heap - Polling O(log(n)), Removing O(n)
Fibonacci Heap
Binomial Heap
Pairing Heap

## Removing Elements From Binary Heap in O(log(n))

## Union Find

Union Find is a data structure that keeps track of elements which are split into one or more disjoint set. Two primary operations: find and union

Use:
Kruskal's minimum spanning tree algorithm
Grid percolation
Network connectivity
Least common ancestor in trees
Image processing.

Application - Kruskal's Minimum Spanning Tree
Given a graph G = (V,E) we want to find a Minimum Spanning Tree in the graph (it may not be unique).
A minimum spanning tree is a subset of the edges which connect all vertices in the graph with the minal total edge cost.
1) sort edges by ascending edge weight
2) walk through the sorted edges and look at the two nodes the edge belongs to , if the nodes are already unified we don't include this edge, otherwise we include it and unify the nodes.
3) the algorithm terminates when every edge has been processed or all the vertices have been unified.

Union and Find Operation
To begin using Union Find, first construct a bijection (a mapping) between your objects and the integers in the range [0, n).
NOTE: This step is not necessary in general, but it will allow us to construct an array-based union find.




