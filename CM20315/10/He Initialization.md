He Initialization assumes you use $\mathrm{ReLU}$.
For the forward pass, the variance of unit activations in layer $k+1$ is the same as in layer $k$:
$$\sigma_\Omega^2 = \frac{2}{\underbrace{D_h}_{\mathclap{\text{Number of units at layer }k}}}$$
Backward pass:
$$\sigma^2_\Omega=\frac{2}{\underbrace{D_{h^\prime}}_{\mathclap{\text{Number of units at layer } k + 1}}}$$
