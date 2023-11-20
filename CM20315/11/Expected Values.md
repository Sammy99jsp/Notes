The expectation of $g[x]$ is the average (mean) value of $g[x]$ when taking the probability distribution of $x$.
$$\mathbb E\Big[\mathrm g\big[x\big]\Big] = \int \mathrm g\big[x\big] \Pr\big(x\big)\mathrm d x$$
We can approximate this by taking a sample $x^\ast_n$ of $x$ values from $\Pr(x)$ and taking an average:
$$\begin{align*}\mathbb E \Big[\mathrm g\big[x\big]\Big] \approx \frac{1}{N} \sum^N_{n=1}g\big[x^\ast_n\big] & & \text{ where }& &x^\ast_n \sim \Pr(x)\end{align*}$$
## Common Expectations
For example:
* $\mathbb E\Big[\mathrm g\big[x\big]\Big] = \mu\ \text{(the mean of g(x))}$
* $\mathbb E \Big[\mathrm g(\big(x\big) - \mu)^2\Big] = \sigma^2 \text{ (the variance)}$   
