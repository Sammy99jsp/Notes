## Naive First Attempt
What if we were to define complexity of a [[Turing Machines|TM]] $M$ is a function $C_M: \mathbb N \mapsto \mathbb N$ such that if $\big| w\big|=n$ then $M$ on input $w$ halts in $C_M(n)$ steps.

But there's a few problems:
- Your TM may not halt on any input $w$!
	- The way we solve this is to pretend this problem does not exist: we assume $M$ will halt for every input.
- Different inputs of the same length may halt in a different number of steps. $|w_1| = |w_2| \cancel{\rightarrow} C_M(w_1) = C_M(w_2)$ 
- This definition is dependent on minor implementation details.