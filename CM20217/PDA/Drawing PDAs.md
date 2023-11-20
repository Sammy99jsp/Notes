### Example 1
Our PDA is formally described as:
- $Q = \big\{1,\ 2,\ 3\big\}$
- $\Sigma = \big\{a,\ b\big\}$
- $\Gamma = \big\{a\big\}$
- $s = 1$
- $F = \big\{1,\ 3\big\}$
- $\Delta$ has:
	- $\big((1,\ a,\ e), \ (2,\ a)\big)$
	- $\big((2,\ a,\ e), \ (2,\ a)\big)$
	- $\big((2,\ b,\ a), \ (3,\ e)\big)$
	- $\big((3,\ b,\ a), \ (3,\ e)\big)$

The diagram looks like:
```tikz
\begin{document}

\begin{tikzpicture}[scale=0.2]
\tikzstyle{every node}+=[inner sep=0pt]
\draw [black] (14.8,-9.4) circle (3);
\draw (14.8,-9.4) node {$1$};
\draw [black] (14.8,-9.4) circle (2.4);
\draw [black] (26.2,-16.9) circle (3);
\draw (26.2,-16.9) node {$2$};
\draw [black] (14.8,-25) circle (3);
\draw (14.8,-25) node {$3$};
\draw [black] (14.8,-25) circle (2.4);
\draw [black] (6.8,-9.4) -- (11.8,-9.4);
\draw (6.3,-9.4) node [left] {};
\fill [black] (11.8,-9.4) -- (11,-8.9) -- (11,-9.9);
\draw [black] (17.389,-26.492) arc (87.78023:-200.21977:2.25);
\draw (16.55,-31.11) node [below] {$b,\ a \rightarrow e$};
\fill [black] (15.19,-27.96) -- (14.66,-28.74) -- (15.66,-28.78);
\draw [black] (23.75,-18.64) -- (17.25,-23.26);
\fill [black] (17.25,-23.26) -- (18.19,-23.21) -- (17.61,-22.39);
\draw (18.5,-20.45) node [above] {$b,\ a \rightarrow e$};
\draw [black] (17.31,-11.05) -- (23.69,-15.25);
\fill [black] (23.69,-15.25) -- (23.3,-14.39) -- (22.75,-15.23);
\draw (15.55,-13.65) node [below] {$a,\ e \rightarrow e$};
\draw [black] (28.02,-14.53) arc (170.20455:-117.79545:2.25);
\draw (32.96,-12.83) node [right] {$a,\ e \rightarrow a$};
\fill [black] (29.19,-16.9) -- (29.89,-17.53) -- (30.06,-16.55);
\end{tikzpicture}
\end{document}
```
Notice how we add the notation $\alpha \rightarrow \beta$ which means $\alpha$ is popped off the stack, then $\beta$ is pushed onto the stack during this transition.











