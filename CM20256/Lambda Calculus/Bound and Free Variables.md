What's the difference $\lambda$-terms $\lambda x.\lambda y.x$ and $\lambda z.\lambda y.z$?
> There isn't, is there?

They do the same thing, but the variables are differently named! In order for us to continue defining $\lambda$-calculus, we need to find a way of figuring out which things are similar, and [[ɑ-conversion|renaming variables]] to make out lives easier.

Let's introduce the concepts of *bound*, and *free* variables.

*Bound* variables belong to some abstraction, such as:
- $k$ in $\lambda k.kk$
- (In higher scopes) $k$ in $\lambda x.\left(\lambda y. \left(\lambda k. kk\right) y\right)x$ 

*Free* variables don't belong to any abstraction:
- $x$ in $\lambda y. x$
- The middle $x$ in the first bracket inside the second bracket: $\left(\lambda x. x x\right)\left(\left(\lambda y. \overset{\downarrow}{x}\right)\left(\lambda x. \lambda y. x\right)\right)$ .

## Definition: Free Variables
The set of free variables $FV(M)$ for some $\lambda$-term $M$ is defined as:
$$\begin{align}FV(x)&=\{x\}\\FV(\lambda x. M)&=FV(M)\ \setminus\ \{x\}\\FV(MN)&=FV(M)\ \cup FV(N)\end{align}$$
