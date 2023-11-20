How do we know which weights $\boldsymbol\Omega_k$ and biases $\boldsymbol\beta_k$ for our neural network.

Well, we can start by setting all the biases to 0: 
$$\boldsymbol\beta_k = \boldsymbol0$$
And, we can normally-distribute our weights according to a binomial distribution:
$$\boldsymbol\Omega_k \sim \mathrm B\big(0,\ \sigma_\Omega^2\big)$$
The problem is:
* We can't make the variance $\sigma^2_\Omega$ too big; and
* We can't make the variance $\sigma^2_\Omega$ too small
Because we will eventually end up at a point where we run out of floating point precision.