Again, let:
$$L_\text{REGEX} = \Big\{\big\langle \alpha,\ w\big\rangle\ \big| \alpha \ \text{is a regular expression describing } w\Big\}$$
### Theorem
$L_{\text{REGEX}}$ is decidable.
#### Proof
On input $\big\langle \alpha,\ w \big\rangle$ do:
1. Convert $\alpha$ to an equivalent NFA $A$ such that $L(\alpha) = L(A)$ using the RegEx->NFA construction.
2. Take any Turing machine deciding $L_{\text{NFA}}$ and run it on input $\big\langle A, w\big\rangle$.  