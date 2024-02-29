This is just the practice of renaming variables.

### Definition: Renaming
We use the notation $M[y / x]$ to mean "replace all $x$ in $M$, with $y$".

We define renaming on our $\lambda$-terms:
$$\begin{align}x[y/x] &= y\\z[y/x]&= z & \text{where } x \neq z\end{align}$$

$$\begin{align}\left(\lambda x. M\right)[y/x] &= \lambda x.M\\\left(\lambda z.M\right)[y/x]&=\lambda z.\left(M[y/x]\right) & \text{where } x \neq z\end{align}$$
> What's with this?

Well, we're only looking at renaming instances of where $x$ is a *free* variable -- since $x$ is bound by an abstraction, we know it can't be free inside $M$.

$$(MN)[y/x]=(M[y/x])(N[y/x])$$
### Definition: ɑ-equivalence
Now that we can rename variables, we can define an equivalence relations between any two $\lambda$-terms.

Two $\lambda$-terms are *alpha-equivalent* $(M =_\alpha N)$ if the $\lambda$-terms only differ in their choice of *bound-variable* names.  