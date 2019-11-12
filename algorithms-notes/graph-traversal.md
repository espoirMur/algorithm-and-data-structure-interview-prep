In this section I will write my take away about graph traversal algorithms

### Depth First Search Algorithm:


This algorithm use a *stack* to keep track of the visited nodes
- we start from a node we mark it as visited, 
From that nodes we takes all the edges and for each edge we check if it's not visited we put it in a stack and we mark it as visited if it's already visited we go to the next contected and not visited


[2 terms](https://www.youtube.com/watch?v=pcKY4hjDrxk)

- Visiting a vertex 
- Exploring a vertex

The rule of Depth first search , is once we have reached a node , we put it in the stack and we explore his children (We prioritize his children we go in deep )

If the child is a leaf node, go in the stack pop the last item and repeat the exploration process


The depth-first algorithm sticks with one path, following that path down a graph structure until it ends.

The depth first search algorithm can help us to determine if a relationship between 2 nodes  exists in a graph.


- Algorithm in deep

We start with a arbitrary node ,



We initialize a set of visited nodes

An empty stack 


Since the stack is empty we put a into the stack and we visit his children

- put each child node we have visited into the stack , once we have reached a leaf node we remove it from the stack and go to the next element and check if it has child others child
We repeat until the stack is empty
