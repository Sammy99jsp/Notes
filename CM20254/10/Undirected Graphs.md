In these graphs, the order of source and target doesn't matter: you can start from either end on an edge.   

```tikz
\begin{document}
	\begin{tikzpicture}
		\node[shape=circle,draw=black] (A) at (0,0) {A};
		\node[shape=circle,draw=black] (B) at (0,3) {B};
		\node[shape=circle,draw=black] (C) at (-3,0) {C};
		\node[shape=circle,draw=black] (D) at (3,0) {D};
		\node[shape=circle,draw=black] (E) at (3,3) {E};
		
		\path [-] (A) edge node {} (B);
		\path [-] (B) edge node {} (C);
		\path [-] (A) edge node {} (D);
		\path [-] (E) edge node {} (D);
		\path [-] (C) edge node {} (A);
		\path [-] (B) edge node {} (E);
		\path [-] (B) edge node {} (D);
	\end{tikzpicture}
\end{document}
```