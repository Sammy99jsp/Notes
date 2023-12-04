- Make a [[Minimum Spanning Trees|minimal spanning tree]] by successively adding edges, each time picking the best candidate (lowest weighted edge that does not create a cycle).
---
```javascript
// Set of edges to consider
S = new Set<Edge>(G.edges)

// New graph with all the vertexes of G, but none of the edges.
T = (new Set<Vertex>(G.vertices), Set<Edge>.empty())

while not S.empty()
	e = S.minimum_cost()
	// If acyclic
	if not T.with(e).is_cyclic()
		T = T.with(e)
```

[[Kruskal's Algorithm - Correctness]]