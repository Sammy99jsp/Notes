What about trying to find a Context-free grammar that accepts
$$L = \Big\{a^n b^n c^n\ \big|\ n \geq 0 \Big\}$$
CFGs work for describing $\big\{a^n b^n\ \big|\ n \geq 0\big\}$ : $s \rightarrow a S b\ \big|\ e$, but there's something about $L$ that makes it not context-free.

Even if we try something like: $$\begin{align*}
	S &\rightarrow aTbVc\ \big| e\\
	T &\rightarrow a T b \big| e\\
	V &\rightarrow b V | e\\
\end{align*}$$
We notice that you can add more $T$s than $V$s, this means that it does not only define $L$, but a super-set containing $L$.