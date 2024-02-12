We can use a concept known as **Entropy**.

## Entropy
Entropy is a measure of how homogeneous (of a similar kind) a dataset is.
$$E(x)=-\sum^{c}_{i=1} P(i) \log_2\left(P(i)\right)$$
where $x$ is some feature with $c$ categories, and $P(i)$ is the probability of an input in the training data being class $i$.
### Information Gain
The information gain $G(x)$ for a feature $x$ is simply the dual of the entropy $G(x) = 1 - E(x)$, and tells us *how useful* 