Trees are a special type of undirected graph which is both connected and acyclic.
```tikz
\begin{document}
	\begin{tikzpicture}
		\node[shape=circle,draw=black] (A) at (0,0) {A};
		\node[shape=circle,draw=black] (B) at (0,3) {B};
		\node[shape=circle,draw=black] (C) at (-3,0) {C};
		\node[shape=circle,draw=black] (D) at (3,0) {D};
		\node[shape=circle,draw=black] (E) at (1.5,-3) {E};
		\node[shape=circle,draw=black] (F) at (4.5,-3) {F};
		
		\path (A) edge node[left] {} (B);
		\path (B) edge node[left] {} (C);
		\path (E) edge node[left] {} (D);
		\path (F) edge node[left] {} (D);
		\path (B) edge node[left] {} (D);
	\end{tikzpicture}
\end{document}
```
### Levels
The *level* of a node is the distance from it and the root node (in this case, $\mathrm A$ is the root node).
### Tree Height
The *height* of a tree is its maximum level.
[[Tree Traversal]]