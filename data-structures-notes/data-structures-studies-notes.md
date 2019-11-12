## What are data structures

Data structures are different way of storing data into a computer.

### Arrays
A sequence of elements looking contiguous in the memory and all elements hold an index.

We can access the element at the index i in  a constant time
Adding an element to the beginning as a linear constant time, because before adding the element to that index we need to move all element to index i+1

### Linked list:

A sequence of element where each element links to the next element.
It can contains duplicates elements for any type. 
It can be sorted or not.
The difference between an array and a linked list is that a linked list does not hold element indexes. But sometimes linked list can associate indexes to elements, it's up to me to design it in that way.

The advantages of a linked list is that insertion and deletion take constant time,but getting an element and adding an element to the end of the list takes linear time.

There is also a double linked list where the element hold the index of the next element and the index of the previous element. 

Sentinel or dummy nodes at head and tail : just for efficiency, and make implementations easier.

### Stacks and Queues

Both stacks and queues are linear data structures, you can both add the element in the same way in both data structures.
The main differences is how elements are removed in them.
We add an element to the top of the 
- A stack is LIFO : last in first out. 
The last element you put in will be the first element to remove.
Ex: Stack of plates in a kitchen
We can push, pop and optionally pop an element to a stack
- A queue is FIFO : First in First Out:
A queue is a line of people entering in a bus for example.

### HashTables


On a hight level a hashtable is a key value look up data structure, key and values can be any type of data structure as long as you have hash functions for keys.

A hash function takes an object of any data type , let say a string convert it into an integer and remap that integer into an index

We map from the key ===> hashcode ===> index

2 strings can have the same hashcode, and 2 strings with differents hashcode can map to the same index, we can that situation collision.

#### How to solve collision?

There are many techniques which help to solve collision when 2 hashcode map to the same index

- Chaining : Use a linked list to save all the values with the same hashcode-index mapping and loop through it when we are performing a searching


#### [More About Hashing](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)

Hashing is a technique that is used to uniquely identify a specific object from a group of similar objects

#### [A better Explanation](https://www.youtube.com/watch?v=KyUTuwz_b7Q)

Remember that when looking for an element in an array if we know the position of the element we can perform the operation in a constant time.

If we don't know the index , it takes a linear time to retrieve an element from a list.

What if we have a function which can give us the element index from the element itself?
So that if we are looking for an element into a list, we convert that element into it index by applying the function and retrieve it by his index in the list.


An example of  hashing algorithm is just an algorithm or a function that take a key a string transform it into a values an integer which is an address where the element is stored in the memory

For number address = key mod n

for string address = assci code of string mod n

where n is the number of all possibles addresses

Collision happens now when after hashing 2 different elements have the same hashing ,

F ex: 8 mod 5 = 3 and 13 mod 5 = 3, this lead to a collision

Open addressing is one of the way to deal with collision, when an item index is already taken , you find the next avialable slot and insert the item there.

when search the item , if the item at the calculated index is different with the item we are looking for, we search to next item until we find the item we are looking for.

A good hash function minimize collision


PS: from what we know, hashing can help us to reduce the number of items we can save, so instead of saving the whole list of items, we can save only indexes generated from the hash function, and can be considered as key fo the hashmap

### [Trees](https://www.freecodecamp.org/news/all-you-need-to-know-about-tree-data-structures-bceacb85490c/)

A tree is an non linear data structure, where data is stored into a hierarchical order.
For example, a family tree, an organization structure, etc.

From a technical perspective, a tree is a collection of entities called *nodes*.
Nodes are connected with each others via *edges* , each node contains values and mau or not have children.

The first node is called the root of the tree, the last node without children are called leaves

Edges are important for a tree because it manages relationship between nodes.

*Height* is the length of the longest path to a leaf

*Depth* is the length of the path to its root

#### Binary tree

A binary tree is a special type of tree where each node has at most 2 children

#### Binary search tree
I a binary tree that follow a specific ordering property.

The left node is less than the root node and less than all the right node.
By analogy to arrays we can say that a binary search tree is just a sorted tree
This make search property fast in a binary search tree.


#### Balanced tree

#### Heaps

A heap is a kinda of tree data structure where the root node is less than all the child nodes for a min heap , or greater than the child nodes for max heap.
Or element in the tree follow just a specific order 


### [Graphs](https://medium.com/basecs/a-gentle-introduction-to-graph-theory-77969829ead8)

A graph is just a collection of nodes, each node may point to another .
They can be directed or undirected :
- They are directed is only one path from node A to node B.
- They are undirected the path that we can travel goes both ways. That is to say, the path between the two nodes is bidirectional, meaning that the origin and destination nodes are not fixed.

Form a mathematic perspective , a graph is just a way to represent a network which is a set of objects that are all interconnected.

#### [Differences between graph and trees](https://freefeast.info/difference-between/difference-between-trees-and-graphs-trees-vs-graphs/)

A graph is different from a tree, a graph doesn't have a root node, there is no such parent child relationship. Any node can have a relationship with any node.

[Trees are nothing more than restricted types of graphs, just with many more rules to follow . A tree will always be a graph, but not all graphs will be trees.](https://medium.com/new-story?inResponseToQuoteId=4776bc537d2d)

