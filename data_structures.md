# Data Structures

* Linear and Non Linear data structures

* Static and Dynamic data structures

* Big O Notation
	- O(1) < O(logn) < O(n) < O(nlogn) < O(n2) < O(n!)
	- https://www.bigocheatsheet.com/
	
* Arrays
	- Row major indexing
	- Column major indexing
	- Add/Remove elements
		- Beginning  - O(n)
		- Middle - O(n)
		- End - O(1)
	- Constant time access
	- Contiguous area of memory
	- Equal size elements (what about unequal?)
	
* Stacks
	- Last In, First Out
	
* Queue
	- First In, First Out
	
* Linked List
	* Singly Linked List
		- Node key and next pointer
	* Doubly Linked List
		- Node key, next and prev pointer
	* Circular Linked List
		- Single or Double, tail points to head

* Trees
	- Root, Link/Edge, Parent, Child, Sibling, Internal, Leaf
	- Depth: number of edges from root
	- Height: number of edges on the longest path to leaf
	- Level: same as depth
	- n nodes => n-1 edges/links
	- Binary Tree
		- Each node can have at most two children
		- at any level, max 2\*\*i children
		- Complete binary tree: all levels except last are filled, at last level all nodes are as left as possible
		- Perfect binary tree: all levels except last are filled. No partials.
		- number of nodes: 2**(h+1) - 1
		- height: log(n+1) - 1
		- Balaced binary tree: the difference between left and right subtree for any node is atmost 1
		- height of an empty tree: -1
		- height a tree with one node: 0
		- array representation of complete binary tree - parent-i : (2*i)+1 & (2*i)+2
	- Binary search tree
		- left subtree is lesser and right subtree is greater
		- should be balanced to maintain O(nlogn) for insertion, deletion and searching.
		- average case: O(logn), worst case (unbalanced): O(n)
	- Heap
		- binary tree where all nodes are in a specific order and it's shape must be complete
		- heap order property - min heap and max heap
		- addition is done only at the left most available sopt in the tree
		
* Links
	- https://medium.com/@vaidehijoshi
	- https://medium.com/basecs
	- https://www.youtube.com/playlist?list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P
	- https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb
	

