# QuickSort

Am learning the quicksort algorithm from [this blog post](https://dev.to/vaidehijoshi/pivoting-to-understand-quicksort-part-1)

## Definition

Quick sort algorithm use divide and conquer technic and choose a pivot point in a collection of 
elements partition the collection around the pivot so that elements lesser than the pivot move before it and elements greater than the pivot are moved after it.

## Guide to implement quick sort

- Choose the pivot , usually the last element of the collection
- Create the left reference pointing to the first element of the collection
- Create the right reference pointing to the last element of the collection (**Not the pivot element**)
- while left reference is less than the pivot,  move the pointer one element to the right,
    while right reference is greater than the pivot , move the pointer one element to the left
- if **both** left reference is greater than the pivot and right reference is smaller than the pivot , swap the elements at the two references.
- Once both left reference and right references are equals swap the pivot with the element at the **left reference**

## Analyis of quick sort algorithms and Big O Notation:
- Quick sort is a divide and conquer algorithm
- it use recursion
- Not stable sorting algorithms
- Time complexity nlog(n) and worst case = n2 (To be demonstrate when learning Big O)
The worst can can be avoid by writing a randomize partition where we choose pivot 

## The code 

An notebook of the python implementation of the code can be found [here](./notebooks/QuickSort.ipynb) and the visualization
of the code execution can be found [here](http://www.pythontutor.com/visualize.html#code=def%20quicksort%28array,%20start_index,%20end_index%29%3A%0A%20%20%20%20%22%22%22%0A%20%20%20%20do%20the%20quicksort%20algorithms%20recursvely%0A%20%20%20%20%22%22%22%0A%20%20%20%20if%20start_index%20%3C%20end_index%3A%0A%20%20%20%20%20%20%20%20pivot_index%20%3D%20partition%28array,%20start_index,%20end_index%29%0A%20%20%20%20%20%20%20%20quicksort%28array,%20start_index,%20pivot_index-1%29%0A%20%20%20%20%20%20%20%20quicksort%28array,%20pivot_index%2B1,%20end_index%29%20%20%20%20%0A%20%20%20%20%20%20%20%20%0Adef%20partition%28array,%20start_index,%20end_index%29%3A%0A%20%20%20%20%22%22%22%0A%20%20%20%20partition%20the%20array%20and%20return%0A%20%20%20%20return%20index%20of%20the%20pivot%0A%20%20%20%20%22%22%22%0A%20%20%20%20pivot%20%3D%20array%5Bend_index%5D%0A%20%20%20%20p_index%20%3D%20start_index%0A%20%20%20%20for%20i%20in%20range%28start_index,%20end_index%29%3A%0A%20%20%20%20%20%20%20%20if%20array%5Bi%5D%20%3C%3D%20pivot%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20array%5Bi%5D,array%5Bp_index%5D%20%3D%20array%5Bp_index%5D,%20array%5Bi%5D%20%23%20swapping%20the%20index%0A%20%20%20%20%20%20%20%20%20%20%20%20p_index%20%2B%3D1%0A%20%20%20%20array%5Bp_index%5D,array%5Bend_index%5D%20%3D%20array%5Bend_index%5D,%20array%5Bp_index%5D%0A%20%20%20%20return%20p_index%0A%20%20%20%20%0Athe_array%20%3D%20%5B7,%202,%201,%206,%208,%205,%203,%204%5D%0Aquicksort%28the_array,%200,%20len%28the_array%29-1%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false)
