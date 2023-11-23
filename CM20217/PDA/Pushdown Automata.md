---
title: Pushdown automata
date: 2023-11-07
slides: https://moodle.bath.ac.uk/mod/resource/view.php?id=1085071
---
## Automata with Memory 
For a language such as $L = \big\{a^nb^n\big| n \geq 0\big\}$, we know that we cannot represent this as a finite automaton (notice the dots):
```tikz
\begin{document}
\begin{tikzpicture}[scale=0.2]
\tikzstyle{every node}+=[inner sep=0pt]
\draw [black] (17.9,-17.1) circle (3);
\draw [black] (17.9,-17.1) circle (2.4);
\draw [black] (28.2,-25) circle (3);
\draw [black] (19.3,-35.5) circle (3);
\draw [black] (19.3,-35.5) circle (2.4);
\draw [black] (38.2,-33.3) circle (3);
\draw [black] (29.8,-43.8) circle (3);
\draw [black] (47.3,-41.9) circle (3);
\draw [black] (39.5,-51.3) circle (3);
\draw [black] (20.28,-18.93) -- (25.82,-23.17);
\fill [black] (25.82,-23.17) -- (25.49,-22.29) -- (24.88,-23.08);
\draw (22.1,-21.55) node [below] {$a$};
\draw [black] (26.26,-27.29) -- (21.24,-33.21);
\fill [black] (21.24,-33.21) -- (22.14,-32.92) -- (21.38,-32.28);
\draw (23.2,-28.81) node [left] {$b$};
\draw [black] (30.51,-26.92) -- (35.89,-31.38);
\fill [black] (35.89,-31.38) -- (35.6,-30.49) -- (34.96,-31.26);
\draw (32.25,-29.64) node [below] {$a$};
\draw [black] (36.33,-35.64) -- (31.67,-41.46);
\fill [black] (31.67,-41.46) -- (32.56,-41.15) -- (31.78,-40.52);
\draw (33.44,-37.13) node [left] {$b$};
\draw [black] (27.45,-41.94) -- (21.65,-37.36);
\fill [black] (21.65,-37.36) -- (21.97,-38.25) -- (22.59,-37.46);
\draw (25.56,-39.15) node [above] {$b$};
\draw [black] (37.13,-49.46) -- (32.17,-45.64);
\fill [black] (32.17,-45.64) -- (32.5,-46.52) -- (33.11,-45.73);
\draw (35.66,-47.05) node [above] {$b$};
\draw [black] (40.38,-35.36) -- (45.12,-39.84);
\fill [black] (45.12,-39.84) -- (44.88,-38.93) -- (44.19,-39.65);
\draw (41.79,-38.08) node [below] {$a$};
\draw [black] (45.38,-44.21) -- (41.42,-48.99);
\fill [black] (41.42,-48.99) -- (42.31,-48.69) -- (41.54,-48.06);
\draw (42.85,-45.16) node [left] {$b$};
\draw (52, -45) node [align=left] {$\ddots$};
\draw (44, -53) node [align=left] {$\ddots$};
\end{tikzpicture}
\end{document}
```
(Start at the top node, whoops!)

We'd need infinite states to keep of how many $a$-s and $b$-s we have!
But, we can make a modification to our automaton in order for it to have finite states: let's add the concept of *stack memory*.
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
\draw (6.3,-9.4) node [left] {Start};
\draw (-18,-10) rectangle ++(20,2) node[pos=.5] {Start with empty stack.};
\draw (6,-15) rectangle ++(12,2) node[pos=.5] {Add $a$ to stack.};
\draw (35,-14) rectangle ++(12,2) node[pos=.5] {Add $a$ to stack.};
\draw (22,-24) rectangle ++(24,2) node[pos=.5] {Remove an $a$ from the stack.};
\draw (22,-32) rectangle ++(24,2) node[pos=.5] {Remove an $a$ from the stack.};
\draw (-14,-25) rectangle ++(24,2) node[pos=.5] {Only accept if stack is empty.};

\fill [black] (11.8,-9.4) -- (11,-8.9) -- (11,-9.9);
\draw [black] (17.389,-26.492) arc (87.78023:-200.21977:2.25);
\draw (19.55,-31.11) node [below] {$b$};
\fill [black] (15.19,-27.96) -- (14.66,-28.74) -- (15.66,-28.78);
\draw [black] (23.75,-18.64) -- (17.25,-23.26);
\fill [black] (17.25,-23.26) -- (18.19,-23.21) -- (17.61,-22.39);
\draw (19.5,-20.45) node [above] {$b$};
\draw [black] (17.31,-11.05) -- (23.69,-15.25);
\fill [black] (23.69,-15.25) -- (23.3,-14.39) -- (22.75,-15.23);
\draw (19.55,-13.65) node [below] {$a$};
\draw [black] (28.02,-14.53) arc (170.20455:-117.79545:2.25);
\draw (32.96,-12.83) node [right] {$a$};
\fill [black] (29.19,-16.9) -- (29.89,-17.53) -- (30.06,-16.55);
\end{tikzpicture}
\end{document}
```

Notice for our word to be accepted, we *start with an empty stack* in the starting state and *end with an empty stack* in an accepting state.

[[CM20217/PDA/Definition]]
[[Accepting Languages]]
[[Drawing PDAs]]