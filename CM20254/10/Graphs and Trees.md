---
title: Graphs and Trees
date: 2023-11-06
url: https://moodle.bath.ac.uk/mod/resource/view.php?id=1269811
reading: https://link.springer.com/content/pdf/10.1007/978-1-4612-0619-4.pdf?pdf=button
---
[[Graphs]]
[[Trees]]

```tikz
\begin{document}
	\begin{tikzpicture}
		\node[shape=circle,draw=black] (B) at (0,0) {B};
		\node[shape=circle,draw=black] (A) at (0,3) {A};
		\node[shape=circle,draw=black] (C) at (-3,0) {C};
		\node[shape=circle,draw=black] (D) at (3,0) {D};
		\node[shape=circle,draw=black] (E) at (4.5,-3) {E};
		\node[shape=circle,draw=black] (F) at (1.5,-3) {F};
		\node[shape=circle,draw=black] (G) at (-3,-3) {G};
		
		\node at (-6,3) {Level 0};
		\node at (-6,0) {Level 1};
		\node at (-6,-3) {Level 2};

		\path (A) edge node[left] {} (B);
		\path (A) edge node[left] {} (D);
		\path (C) edge node[left] {} (A);
		\path (D) edge node[left] {} (E);
		\path (D) edge node[left] {} (F);
		\path (C) edge node[left] {} (G);
	\end{tikzpicture}
\end{document}
```















