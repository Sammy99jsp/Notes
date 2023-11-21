This is a method to convert a context-free grammar to a PDA:

> Let $G = \big(\Sigma,\ V,\ R,\ S\big)$ be a context-free grammar.
> Define the push-down automaton $A = \big(Q,\ \Sigma,\ \Gamma,\ s,\ \Delta,\ F\big)$ as:
>* $Q = \big\{1,\ 2\big\}$
>* $\Gamma = \Sigma \cup V$
>* $s = 1$
>* $F = \big\{2\big\}$
>* $\Delta$ is given by:
	* $\big((1, e, e),\ (2, S)\big)$
	* $\big((2, e, X),\ (2, w)\big)$ for each $X\rightarrow w$ in $R$ 
	* $\big((2, a, a),\ (2, e)\big)$ for each $a \in \Sigma$
	
```tikz
\begin{document}
\begin{tikzpicture}[scale=0.2]
\tikzstyle{every node}+=[inner sep=0pt]
\draw [black] (25.7,-12.4) circle (3);
\draw (25.7,-12.4) node {$1$};
\draw [black] (45.3,-12.4) circle (3);
\draw (45.3,-12.4) node {$2$};
\draw [black] (45.3,-12.4) circle (2.4);
\draw [black] (19.5,-12.4) -- (22.7,-12.4);
\fill [black] (22.7,-12.4) -- (21.9,-11.9) -- (21.9,-12.9);
\draw [black] (28.7,-12.4) -- (42.3,-12.4);
\fill [black] (42.3,-12.4) -- (41.5,-11.9) -- (41.5,-12.9);
\draw (35.5,-12.9) node [below] {$e,\ e \rightarrow S$};
\draw [black] (46.623,-15.08) arc (54:-234:2.25);
\draw (45.3,-19.65) node [below] {$e,\ X \rightarrow w$};
\fill [black] (43.98,-15.08) -- (43.1,-15.43) -- (43.91,-16.02);
\draw [black] (43.977,-9.72) arc (234:-54:2.25);
\draw (45.3,-5.15) node [above] {$a,\ a \rightarrow e$};
\fill [black] (46.62,-9.72) -- (47.5,-9.37) -- (46.69,-8.78);
\end{tikzpicture}
\end{document}
```
>Then $L(A) = L(G)$ 

Here, we're essentially:
1. Adding a starting variable $S$ to the stack. 
2. Implementing the left-most derivation $S \Rightarrow^\ast w$ (replace the left-most variable with a word)
3. Whenever a terminal (a letter) appears on the top of the stack, it should match the next letter of the input word $w$,