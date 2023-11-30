Let $L_{\text{TM}} = \Big\{\big\langle M, \ w\big\rangle \big| M\ \text{is a Turing machine and } M \text{ halts on } W \Big\}$
### Theorem
$L_{\text{LM}}$ is semi-decidable.
#### Proof
On input $\big\langle M,\ w\big\rangle$:
1. Run $M$ on input $w$ (the next step in the computation is always exactly determined).
2. If $M$ halts on $w$, then halt.