We can't use fully-connected networks as:
1. Images contain masses of data (think about the fact that every RGB sub-pixel in an image count as a dimension for our input).
	- Hidden Layers are generally more numerous than input dimensions
2. Nearby pixels are statistically related
	- It's likely that one pixel will correlate with its neighbours.
3. We want our model to be stable under transformations
	- As in, "a tree is still a tree, no matter if it's on the left, or the right of the image".

## Properties we want
### Invariance
We want the model $\boldsymbol{\mathrm f}[\boldsymbol{\mathrm x}]$ to be invariant to a transformation $\boldsymbol{\mathrm t}[\boldsymbol{\mathrm x}]$, as in:
$$\boldsymbol{\mathrm f}\big[\boldsymbol{\mathrm t}[\boldsymbol{\mathrm x}]\big] = \boldsymbol{\mathrm f}\big[\boldsymbol{\mathrm x}\big]$$

Introducing [[Convolutional Networks]]