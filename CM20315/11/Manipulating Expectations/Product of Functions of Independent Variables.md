Here, we need to use two *independent* variables $x, y$ as $\Pr\big(x, y\big) = \Pr\big(x\big)\Pr\big(y\big)$.

$$\begin{align*}
	\mathbb E \Big[\mathrm f\big[x\big] \cdot \mathrm g\big[y\big]\Big] &= {\large\iint} \mathrm f\big[x\big] \cdot \mathrm g\big[y\big]\Pr\big(x, y\big)\mathrm dx\mathrm dy\\
	&= {\large \iint}\mathrm f\big[x\big] \cdot \mathrm g\big[y\big]\underbrace{\Pr\big(x\big)\Pr\big(y\big)}_{\mathclap{\text{as } x,\ y \text{ are independent}}} \mathrm dx\mathrm dy\\
	&= \int\mathrm f\big[x\big]\Pr\big(x\big)\mathrm d x \int\mathrm g\big[y\big]\Pr\big(y\big)\mathrm d y\\
	&= \mathbb E\Big[\mathrm f\big[x\big]\Big] \mathbb E\Big[\mathrm g\big[y\big]\Big]
\end{align*}$$
