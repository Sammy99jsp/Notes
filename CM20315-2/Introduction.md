---
slides: https://moodle.bath.ac.uk/mod/resource/view.php?id=1285640
---
## Hypothesis Notation
We can think of our model as a hypothesis for what an output could be under parameters $\theta$ for input $x$:
$$h_{\theta}(x) = \theta_0 + \theta_1 x$$
## Cost Functions
These can be thought of as a loss function:
$$J(\theta) = \frac{1}{2m}\sum_{i=1}^{m}\Big(h_\theta(x^i) - y^i\Big)^2$$[Notation]