A PDA $A$ accepts a corresponding language $L(A)$.
1. Let $A = \big(Q,\ \Sigma,\ \Gamma,\ s,\ \Delta,\ F\big)$ be a PDA.

   We can say that $A$ accepts $w \in \Sigma^\ast$ if $(s,\ w,\ e)$ [[Computation|yields]] $(q,\ e,\ e)$ for some $q \in F$.

	This is a formal way of saying that a word is accepted if we can start in the starting state with an empty stack, follow a path through the automaton ending up at an accepting state with an empty stack. 