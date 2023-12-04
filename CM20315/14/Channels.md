As convolution reduces the amount of information quite drastically - we can perform multiple convolutions at once, looking at different regions of the input, and stack them in *channels*.

Below shows a one input/two output channel layer:
![[channels-img.png]]

Notice how the weights are different when convolving the second channel in (b).

We can map from any number of input channels to output channels in our convolutional layer when using:
$$\boldsymbol\Omega \in \mathbb{R}^{(\overset{\textnumero\ \text{Input channels}}{C_i} \times \overset{\textnumero\ \text{Output channels}}{C_o}\times \overset{\text{Kernel size}}{K})}$$