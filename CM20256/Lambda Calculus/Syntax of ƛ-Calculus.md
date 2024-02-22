## Syntax Definition: $\lambda$-terms
We define $\lambda$-term $M$ by the definition:
$$M ::= x\ |\ \lambda x . M\ |\ MM$$
where $x$ ranges over an infinite collection of variables.
(This type of definition is known as a Backus-Normal Form grammar, or BNF).
#### What?
| $\lambda$- term | Definition |
| ---- | ---- |
| Variable $x$ | $x$ is some variable. |
| Abstraction $\lambda x. M$ | You can think of $\lambda x. M$ as a function where, given argument x, behaves like $M$.<br><br>When you bind $x$ as an argument $M$ will be "evaluated": $(\lambda x.M) x$ will yield $M$. |
| Application $M_1 . M_2$ | Function application, apply $M_1$ to $M_2$.  |
### Bracketing
- Application is *left-associative*: $MNP$ is equivalent to $(MN)P$.
- The scope of $\lambda$ extends as far right as possible, before hitting the end, or a $)$: $\lambda x.MN$ is equivalent to $\lambda x. (MN)$, *not* $(\lambda x. M)N$.
- For multiple variables, $\lambda x y . M$ can be written as shorthand for $\lambda x. \lambda y. M$ . Sometimes, the dot is even omitted.
### Syntax Trees
We can parse any valid $\lambda$-term with our formal syntax and turn it into a tree:
#### Single Variable

```tikz
\usepackage{tikz}
\usetikzlibrary{trees}
\begin{document}
\begin{tikzpicture}[level distance=1.5cm, every node/.style={scale=2.0}]
  \node {$x$};
\end{tikzpicture}
\end{document}
```

#### Abstraction
```tikz
\usepackage{tikz}
\usetikzlibrary{trees}
\begin{document}
\begin{tikzpicture}[level distance=1.5cm, every node/.style={scale=2.0}]
  \node {$\lambda$}
    child {
	  node{x}
    }
    child {
      node{M}
    };
\end{tikzpicture}
\end{document}
```

#### Application
Note that sometimes, 'apply' is just written as $@$.
```tikz
\usepackage{tikz}
\usetikzlibrary{trees}
\begin{document}
\begin{tikzpicture}[level distance=1.5cm, every node/.style={scale=2.0}]
  \node {apply}
    child {
	  node{x}
    }
    child {
      node{M}
    };
\end{tikzpicture}
\end{document}
```
#### More Complicated example
Take the term $\lambda f.\lambda x.\left(f \left(f x\right)\right)$:
```tikz
\usepackage{tikz}
\usetikzlibrary{trees}
\begin{document}
\begin{tikzpicture}[level distance=1.5cm, every node/.style={scale=2.0}]
  \node {$\lambda$}
    child {
	  node{$f$}
    }
    child {
      node{$\lambda$}
        child {
          node{$x$}
        }
        child {
          node{$@$}
            child {
              node{$f$}
            }
            child {
	          node{$@$}
	            child {
	              node{$f$}
	            }
	            child {
	              node{$x$}
	            }
            }
        }
    };
\end{tikzpicture}
\end{document}
```

