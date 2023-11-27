## Initialisation
- $d(s)= 0$ and $d(u) = \infty$ for all $u \neq s$
- $S = \emptyset$
- $Q = V$ where $Q$ is a priority queue ordered by the least current estimate $d$.
## Algorithm
```
while (Q not empty) { 
	get u from Q; // get lowest-weighted vertex
	add u to S; // u is settled!!
	for (v adjacent to u) { 
		if ( d(v) > d(u) + w(u,v) ) { // path via u is shorter 
			d(v) = d(u) + w(u,v); // update estimate for u 
		} 
	}
}
```