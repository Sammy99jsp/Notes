---
slides: https://moodle.bath.ac.uk/mod/resource/view.php?id=1277839
---
## The Problem to Solve
We're given a directed graph with vertices $V$ and edges $E$, with at most one edge between any pair of vertices.

Each edge has a weight attached to it. If we define a weight function that encompasses any pair of vertices:
- The pair with an edge connecting them will have a finite weight attached to it.
- Any pair without an edge connecting them has a weight of $\infty$.

A path along a graph $u \rightarrow v_1 \rightarrow \dots \rightarrow v_n \rightarrow v$ between $u$ and $v$, we define the weight of this path to be the sum of the weights of the edges:
$$w(u \rightarrow v)= w(u \rightarrow v_1) + \dots + w(v_{n-1} \rightarrow v_n) + w(v_n \rightarrow v)$$
We want to find the shortest path between these vertices.

### Algorithms
[[]]