Let $L_\text{NFA} = \Big\{\big\langle A,\ w\big\rangle\ \big| A\ \text{is a NFA and } A\ \text{accepts }w\Big\}$
### Theorem
$L_{\text{NFA}}$ is decidable.
#### Proof
On input $\big\langle A,\ w\big\rangle$ :
1. Convert $A$ to an equivalent DFA $A^\prime$ using the powerset construction.
2. Follow the proof for [[Computing DFAs with TMs||DFAs]]
