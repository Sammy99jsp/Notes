A max-heap is a binary tree that's optimised for storing priority queues.

Specifically: A max-heap is a binary tree that's:
- **Complete**: All levels but the last are fully filled, and the last level is filled left-to-right.
- Has the **max-heap property** - every node is larger than any node in its sub-trees.

A valid max-heap:

```tikz
\usepackage{tikz}
\usetikzlibrary{trees}
\begin{document}
\begin{tikzpicture}[level distance=1.5cm,
  level 1/.style={sibling distance=3cm},
  level 2/.style={sibling distance=1.5cm}]
  \node {25}
    child {node {17}
      child {
	    node {12}
		    child {
		      node {4}
		    }
		    child {
		      node {9}
		    }
		}
		
      child {
	    node {8}
	    }
	  }
    child {
	    node {10}
	    child {
		    node {5}
		}
	    child {
		    node {1}
		}
    };
\end{tikzpicture}
\end{document}
```











