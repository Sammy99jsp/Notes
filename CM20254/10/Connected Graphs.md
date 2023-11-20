Connected graphs are undirected graphs where there is  a path from any node to any other node.
```tikz
\begin{document}
	\begin{tikzpicture}
		\node[shape=circle,draw=black] (A) at (0,0) {A};
		\node[shape=circle,draw=black] (B) at (0,3) {B};
		\node[shape=circle,draw=black] (D) at (3,0) {D};
		\node[shape=circle,draw=black] (E) at (3,3) {E};
		
		\path [draw=red] (A) edge node[left] {} (B);
		\path (A) [draw=red] edge node[left] {} (D);
		\path (E) edge node[left] {} (D);
		\path (B) edge node[left] {} (E);
		\path (A) [draw=red] edge node[left] {} (E);
	\end{tikzpicture}
\end{document}
```
