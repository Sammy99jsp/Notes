> 1. Create a complete tree containing elements of input collection $C$ in any order.
		- $O(n)$ complexity.
> 2. Starting from the bottom-up, sift every element down.
		- $O(n)$ complexity.
> 3. Repeatedly perform [[getMax]] and [[deleteMax]] to retrieve the elements in the correct order.
		- $O(n \log n)$ complexity

Therefore, total complxity of 