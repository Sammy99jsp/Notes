A language $L \subseteq \big(\Sigma_0\big)^\ast$ is called **semi-decidable** if there is a TM $M$ with input alphabet $\Sigma_0$ such that:
- if $w \in L$, then $M$ halts on $w$;
- if $w \notin L$, then $M$ doesn't halt on $w$.