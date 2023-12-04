> Construct a minimal spanning tree by successively adding edges, each time selecting the best candidate (lowest weight edge which doesn't create a cycle).
---
```javascript
// Edges to consider.
S = new Set<Edge>(...)
				  
// New graph with vertices and no edges.
T = (Set<Vertex>.empty(...),Set<Edge>.empty()) 

while not S.is_empty()
	e = S.pop_minimal() // 'Pop' the minimal cost edge.
	if not T.with(e).is_cyclic() // If T+e is acyclic
		T = T.with(e)	
```

You may notice, that this algorithm always takes the best choice presented to it (least costly weight), which puts it in the class of **greedy algorithms**.
