This proof is a bit of a doozy.

Here, we're using the following loop invariant:
> The graph $T$ is acyclic and can be extended (by potentially adding more edges) to a minimum spanning tree of $G$.

### Start of the loop
The invariant is clearly held when $T$ is initialised to have no edges.
### During the loop
Let's make $e$ the minimum cost edge.
* Let $T^\prime$ be an MST that extends $T$, and consider $T^\prime \cup \big\{e\big\}$.
	* If $T^\prime$ contains $e$, then it's also an extension of $T + \big\{e\big\}$, so the invariant still holds.
	* **Assume** that $T^\prime$ 
### Exiting the loop
- At this point, there are new edges that could be added to $T$ without creating a cycle.
- Since the by loop invariant $T$ can be extended to a MST but we can't add an edge at this point, then $T$ itself must be the MST.