Let $M = \big(Q,\ \Sigma,\ \Sigma_0,\ s,\ \delta,\ H\big)$ be a TM:#.
A **configuration** in a TM is a tuple $(q,\ u,\ a,\ v)$ where $q \in Q;\ u, v \in \Sigma^\ast;\ \text{and } a \in \Sigma$, such that $uav$ is a word starting with $\triangleright$.

This is often abbreviated  as $\overset{\mathclap{\begin{array}{c}\text{before head}\\| \\\downarrow\end{array}}}{u}\underset{\mathclap{\begin{array}{c}\uparrow\\\text{head state}\end{array}}}{q}\overbrace{av}^{\mathclap{\hphantom{25em}\text{at and after head}}}$, where $u$ is the tape before the head, $q$ is the state of the head, and $a$ is the state at the head, and $v$ is the tape after the head.

It is said that for $b \in \Sigma$ :

(Here, I've put sets $u$ and $v$ **in bold** to differentiate them as array-like things).

- $uqav$ yields $upbv$ in one step if $\delta(q,\ a) = (p,\ b)$ 
	- AKA: *Rewrite the the current cell with value $b$:*
$$\boldsymbol u\ \overset{\mathclap{\begin{array}{c}q\\\downarrow\end{array}}}{a\vphantom{23em}}\ \boldsymbol v \longrightarrow \boldsymbol u\ \overset{\mathclap{\begin{array}{c}p\\\downarrow\end{array}}}{b}\ \boldsymbol v $$
- $ubqav$ yields $upbav$ in one step if $\delta(q,\ a) = (p,\ L)$
	- AKA: *Move left*
$$\boldsymbol u\ b\ \overset{\mathclap{\begin{array}{c}q \\ \downarrow\end{array}}}{a\vphantom{2.5em}}\ \boldsymbol v
\longrightarrow 
\boldsymbol u\ \overset{\mathclap{\begin{array}{c}p \\ \downarrow\end{array}}}{b\vphantom{2.5em}}\ a\ \boldsymbol v$$
- $uqabv$ yields $uapbv$ in one step if $\delta(q,\ a) = (p,\ R)$
	- AKA: *Move right*
$$\boldsymbol u\ \overset{\mathclap{\begin{array}{c}q \\ \downarrow\end{array}}}{a\vphantom{2.5em}}\ b\ \boldsymbol v
\longrightarrow 
\boldsymbol u\ a\ \overset{\mathclap{\begin{array}{c}p \\ \downarrow\end{array}}}{b\vphantom{2.5em}}\ \boldsymbol v$$