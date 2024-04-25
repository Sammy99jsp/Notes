Given some $\lambda$-term, can you give it a type?

### An informal approach
1. Build the typing derivation without filling the types.
2. Fill in types according to:
	1. Give each term a type variable
	2. If you have a type variable $\alpha$, but you need an arrow type (for a function), make the type $\beta \rightarrow \gamma$ (where $\beta$ and $\gamma$ are new type variables).
	3. If you have type variable $\alpha$, but you need a different type $\tau$ that **does not contain $\alpha$**, replace $\alpha$ with $\tau$.