### What?
- It finds the weight of the shortest path from a source vertex $s$ to any other vertex $u$. 
- It can easily be adapted to store the path information and therefore return the shortest path *(assuming there are no negative weights)*.
### How?
- Let $\delta(u)$ be the weight of the shortest path from $s$ to $u$.
- Make a table mapping distance estimates $d(u)$ for each vertex $u$.
	- Initially set $d(s)=0$ and $d(u) = \infty$ where $s \neq u$ (every other node).
- Explore the graph, and build a set $S$ of *settled vertices*. Initially, $S = \emptyset$.
	- Every time we add a vertex $u$ to $S$, we improve our distance estimate.
- We always add the next vertex representing the shortest possible extension. Because of this, we can prove that $d(u)=\delta(u)$ for all $u \in S$.
- At the end, $S = V$ which means we're done!

[[Dijkstra Pseudocode]]
[[Dijkstra Correctness]]