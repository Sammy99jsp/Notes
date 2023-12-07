---
slides: https://moodle.bath.ac.uk/mod/resource/view.php?id=1094546
---

Intuitively, when thinking of the [[Turing Machines|Turing machine]], the complexity of any algorithm is the number of steps to halt by its corresponding Turing machine.

## Examples
Remember that $L$ and $R$ are reserved for *go left* and *go right* respectively.
Notice that $\triangleright \rightarrow R$  is implicitly part of these TMs.
### Example 1
Let $M_1$ be the the Turing machine that deletes all of its input:

```tikz
\usepackage{tikz}

\begin{document}

\begin{tikzpicture}[scale=0.2]
\tikzstyle{every node}+=[inner sep=0pt]
\draw [black] (25.7,-12.4) circle (3);
\draw (25.7,-12.4) node {$s$};
\draw [black] (45.3,-12.4) circle (3);
\draw (45.3,-12.4) node {$q$};
\draw [black] (45.3,-12.4) circle (2.4);
\draw [black] (25.7,-25.1) circle (3);
\draw (25.7,-25.1) node {$h$};
\draw [black] (25.7,-25.1) circle (2.4);
\draw [black] (19.5,-12.4) -- (22.7,-12.4);
\fill [black] (22.7,-12.4) -- (21.9,-11.9) -- (21.9,-12.9);
\draw [black] (27.61,-10.097) arc (132.91312:47.08688:11.588);
\fill [black] (43.39,-10.1) -- (43.14,-9.19) -- (42.46,-9.92);
\draw (35.5,-6.5) node [above] {$a\rightarrow\sqcup$};
\draw [black] (43.567,-14.838) arc (-43.1706:-136.8294:11.062);
\fill [black] (27.43,-14.84) -- (27.62,-15.76) -- (28.34,-15.08);
\draw (35.5,-18.83) node [below] {$\sqcup\rightarrow R$};
\draw [black] (42.3,-12.4) -- (28.7,-12.4);
\fill [black] (28.7,-12.4) -- (29.5,-12.9) -- (29.5,-11.9);
\draw (35.5,-11.9) node [above] {$a\rightarrow a$};
\draw [black] (25.7,-15.4) -- (25.7,-22.1);
\fill [black] (25.7,-22.1) -- (26.2,-21.3) -- (25.2,-21.3);
\draw (25.2,-18.75) node [left] {$\sqcup \rightarrow \sqcup$};
\end{tikzpicture}

\end{document}
```
We can see here that for any input word of form $a^n$, then our machine is going to to take $(\underset{s \rightarrow q}{n} + \underset{q \rightarrow s}{n} + \underset{s \rightarrow h}{1}) = 2n + 1$ steps for input length $\big |a^n \big| = n$.

### Example 2
Let $M_2$ be the Turing machine that determines whether a stack of $a$-s is odd or even:
```tikz
\usepackage{tikz}

\begin{document}
\begin{tikzpicture}[scale=0.2]
\tikzstyle{every node}+=[inner sep=0pt]
\draw [black] (25.7,-12.4) circle (3);
\draw (25.7,-12.4) node {$s$};
\draw [black] (45.3,-12.4) circle (3);
\draw (45.3,-12.4) node {$q$};
\draw [black] (45.3,-12.4) circle (2.4);
\draw [black] (25.7,-25.1) circle (3);
\draw (25.7,-25.1) node {$e$};
\draw [black] (25.7,-25.1) circle (2.4);
\draw [black] (45.3,-25.1) circle (3);
\draw (45.3,-25.1) node {$o$};
\draw [black] (45.3,-25.1) circle (2.4);
\draw [black] (19.5,-12.4) -- (22.7,-12.4);
\fill [black] (22.7,-12.4) -- (21.9,-11.9) -- (21.9,-12.9);
\draw [black] (27.61,-10.097) arc (132.91312:47.08688:11.588);
\fill [black] (43.39,-10.1) -- (43.14,-9.19) -- (42.46,-9.92);
\draw (35.5,-6.5) node [above] {$a
\rightarrow R$};
\draw [black] (43.567,-14.838) arc (-43.1706:-136.8294:11.062);
\fill [black] (27.43,-14.84) -- (27.62,-15.76) -- (28.34,-15.08);
\draw (35.5,-18.83) node [below] {$a \rightarrow R$};
\draw [black] (25.7,-15.4) -- (25.7,-22.1);
\fill [black] (25.7,-22.1) -- (26.2,-21.3) -- (25.2,-21.3);
\draw (25.2,-18.75) node [left] {$\sqcup \rightarrow \sqcup$};
\draw [black] (45.3,-15.4) -- (45.3,-22.1);
\fill [black] (45.3,-22.1) -- (45.8,-21.3) -- (44.8,-21.3);
\draw (45.8,-18.75) node [right] {$\sqcup \rightarrow \sqcup$};
\end{tikzpicture}
\end{document}
```

Here, for an input $a^n$, you see we take $n+1$ steps, so we can measure the 'complexity' as $n \mapsto n+1$.
