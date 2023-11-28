$$\hat{\boldsymbol\phi}= \underset{\boldsymbol\phi}{\mathrm{argmin}}\left[\mathrm L\left[\boldsymbol\phi, \left\{\boldsymbol{\mathrm{x}}_i,\ \boldsymbol{\mathrm{y}}_i\right\}\right] + \lambda \sum_j (\phi_j)^2\right]$$
Also known as Tikhonov regularisation, or ridge regression.
This is typically only used for weights in NNs - this is known as *weight decay*.

This technique:
- Discourages adherence to data (over-fitting).
- Encourages smoothness between datapoints.