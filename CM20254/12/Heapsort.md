The main idea is *sorting by priority*:
1. Get the biggest item (highest priority) from an unsorted part of the array, and move yo the start of a sorted part.
2. Continue until the unsorted part is empty.

Heapsort does this cleverly, by utilising the [[Max-heap]] data structure.
***
**Input**: Some collection $C$
1. Create a heap (using *make-heap*\*) containing the elements of $C$.
2. Repeatedly perform [[getMax]] and [[deleteMax]] to retrieve the elements in the correct order.
***
**make-heap**
1. Create a complete tree containing the elements of $C$ in any arbitrary order.
2. Starting from the lower level and working up: sift every element down.
[[Make-heap complexity]]
