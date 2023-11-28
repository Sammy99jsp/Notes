Here, we modify the loss function using various gradient descent techniques:
### Gradient Descent
$$\tilde{\mathrm L}_{GD}\big[\boldsymbol\phi\big]+\frac{\alpha}{4}\Bigg\|\frac{\partial L}{\partial \boldsymbol\phi}\Bigg\|^2$$
The above disfavours areas where gradients are steep.
### Stochastic Gradient Descent
$$\tilde{\mathrm L}_{SGD}\big[\boldsymbol\phi\big]=\tilde{\mathrm L}_{GD}\big[\boldsymbol\phi\big] + \frac{\alpha}{4B}\sum_{b=1}^B \Bigg\|\frac{\partial L_b}{\partial \boldsymbol\phi}- \frac{\partial L}{\partial \boldsymbol\phi}\Bigg\|^2$$
Here, we favour batches with similar gradients to each other.

These all depend on the learning rate $\alpha$.

Generally performance is best with:
- Larger $\alpha$ learning rates.
- Best with smaller batch sizes.
