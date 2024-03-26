### Boo-leans!
In order for branching, we need our boolean constants `true` and `false`.

We can encode this with lambda terms too!
$$\begin{align}\text{true} &\triangleq \lambda x.\lambda y.x\\\text{false}&\triangleq \lambda x.\lambda y. y\end{align}$$

We can use beta-reduction to see that $\text{true}\ M\ N \rightarrow_{\beta}^{\ast} M$.

### If
Let's make branching now, with a function called `ifthen`:
$$\text{ifthen} \triangleq \lambda b.\lambda x.\lambda y. b\ x\ y$$
You can see that this works out really nicely when you $\beta$-reduce (since $\text{true}$ returns the first argument, and $\text{false}$ returns the second).

Now that we have branching and booleans, we can define our boolean operations.
### And 
$$\text{and} \triangleq \lambda b_1.\lambda_2.\text{ifthen}\  b_1\ b_2\ \text{false}$$
### Or
$$\text{or} \triangleq \lambda b_1.\lambda_2.\text{ifthen}\  b_1\ \text{true}\ b_2$$
