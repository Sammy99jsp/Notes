This is a technique that modern deep learning frameworks (such as PyTorch).

Essentially, it makes every component of your model (such as the $\mathrm{ReLU}$ function) responsible for computing its own derivative - for example, a linear function responsible for a hidden layer knows how to compute its output's derivative with respect to its inputs, or parameters.