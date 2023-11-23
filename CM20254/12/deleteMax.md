When we remove the root, we need to restructure our tree such that the hierarchy (the Max-heap property) is conserved.

To do this, we:
1. Find the last element in the bottom, and put it at the root.
2. Sift it *down*, if necessary:
	1. Compare the element to its children.
	2. If it is smaller than one of them, swap it with its larger child, and repeat this sifting down the tree if required.