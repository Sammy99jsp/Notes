For a PDA $A = \big(Q, \Sigma, \Gamma, s, \Delta, F\big)$:
* A triple $(p, w, \gamma) \in Q \times \Sigma^\ast \times \Gamma^\ast$  is known as a **configuration** of $A$.
	
	We can think of a configuration as the status of $A$ at any one time: it incorporates:
	* Current state $p$ 
	* Input word left to read $w$
	* Current content of the stack $\gamma$
	* 