Cycles are paths made of *distinct* edges that starts and ends at the same node.
```tikz
\begin{document}
	\begin{tikzpicture}
		\node[shape=circle,draw=black] (A) at (0,0) {A};
		\node[shape=circle,draw=black] (B) at (0,3) {B};
		\node[shape=circle,draw=black] (C) at (-3,0) {C};
		\node[shape=circle,draw=black] (D) at (3,0) {D};
		\node[shape=circle,draw=black] (E) at (3,3) {E};
		
		\path [->] [draw=red] (A) edge node[left] {$1$} (B);
		\path [->] [draw=red] (B) edge node[left] {$\sqrt 2$} (C);
		\path [->] (A) edge node[left] {$3$} (D);
		\path [<-] (E) edge node[left] {$\frac{3}{5}$} (D);
		\path [<-] [draw=red] (C) edge node[left] {$1$} (A);
		\path [<-] (B) edge node[left] {$e$} (E);
		\path [->] (B) edge node[left] {$\pi$} (D);
	\end{tikzpicture}
\end{document}
```
**Note**: Cycles cannot share the same edge. This is not valid:
```tikz
\begin{document}
	\begin{tikzpicture}
		\node[shape=circle,draw=black] (A) at (0,0) {A};
		\node[shape=circle,draw=black] (B) at (0,3) {B};
		
		\path [] [draw=red] (A) edge node[left] {} (B);
	\end{tikzpicture}
\end{document}
```
