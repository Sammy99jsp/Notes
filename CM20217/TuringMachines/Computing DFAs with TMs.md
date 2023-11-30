Let $L_\text{DFA} = \Big\{\big\langle A,\ w\big\rangle\ \big| A\ \text{is a DFA and } A\ \text{accepts }w\Big\}$
### Theorem
$L_{\text{DFA}}$ is [[Decidable|decidable]].
#### Proof
On input $\big\langle A,\ w\big\rangle$ :
1. Run $A$ on input $w$ (as every next step in the automaton is always determined).
2. If we end in an accepting state return $\text{yes}$, otherwise then return $\text{no}$.