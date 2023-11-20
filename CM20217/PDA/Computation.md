For a PDA $A = \big(Q, \Sigma, \Gamma, s, \Delta, F\big)$:
1. A [[Configuration]] $(p,\ av,\ \gamma)$ **yields** another configuration $(q,\ v,\ \delta)$ **in one step** if there exists $\alpha,\ \beta,\ \theta \in \Gamma^\ast$ such that:
	* $\gamma = \alpha \theta$ ($\alpha$ at the top of the stack, followed by $\theta$)
	* $\delta = \beta\theta$ ($\alpha$ popped, then $\beta$ pushed to the top of the stack)
	* $\big((p,\ a,\ \alpha),\ (q,\ \beta)\big)\in \Delta$ (this transition is actually defined in the PDA).
2. If $C_1,\ \dots,\ C_n$ are configurations such that $C_i$ **yields** $C_{i+1}$ in one step for all $i = 1,\ \dots,\ n-1$, we say that $C_1$ yields $C_n$ (i.e. we can follow along a path from $C_1$ to $C_n$ ).