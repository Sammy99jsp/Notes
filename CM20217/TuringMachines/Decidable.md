A language $L \subseteq \big(\Sigma_0\big)^\ast$ is called **decidable** if there is a TM $M$ with input alphabet $\Sigma_0$  and $H = \big\{y,\ n\big\}$such that:
- if $w \in L$, then $M$ halts on $w$ in state $y$;
- if $w \notin L$, then $M$ halts on $w$ in state $n$.
## Theorem
> $L$ is decidable *if and only if* both $L$ and $\big(\Sigma_0\big)^\ast \setminus L$ are semi-decidable - as $w^\prime \notin L \rightarrow w^\prime \in \Big(\big(\Sigma_0\big)^\ast \setminus L\Big)$.