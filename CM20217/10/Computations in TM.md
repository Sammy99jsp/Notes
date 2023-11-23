We say that $M$ *halts* on input word $w \in \big(\Sigma_0\big)^\ast$ if there exists a sequence of configurations $C_1,\ \dots,\ C_n$ such that:
1. $C_1 = \triangleright s w_1 \dots w_n$ (or $C_1 = \triangleright \sqcup$ if $w = e$);
$$\triangleright\ \overset{\mathclap{\vphantom{\Bigg()}\begin{array}{c}q\\\downarrow\\\end{array}}}{w_1}\ \dots\ w_n$$
	*We start in state $s$.*
	
2. $C_i$ yields $C_{i+1}$ in [[Configurations|one step]]  for $i = 1,\ \dots,\ n-1$;
	 *We can follow along the computation step-wise until...*
	 
3. $C_n = uqav$ for $q \in H$
	*We end up in a halting state.*

On input $w \in \big(\Sigma_0\big)^\ast$  there are two possibilities:
1. $M$ halts on $w$; or
2. $M$ runs forever.