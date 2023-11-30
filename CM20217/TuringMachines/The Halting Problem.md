### Theorem
$L_{\text{TM}}$ is not (and cannot be) decidable.
#### Proof
Suppose, for our proof by contradiction, that there is some Turing machine $M_0$ that decides $L_{\text{TM}}$ (can determine if a Turing machine halts).

   Then, let's define another machine $M_1$ on input $\langle M \rangle$:
   - run $M_0$ on input $\big\langle M,\ \langle M\rangle\big\rangle$
   - if $M_0$ halts in $\text{yes}$, loop forever
   - if $M_1$ halts in $\text{no}$, halt in a state $\text{stop}$.

   The idea is that we set up $M_1$ to halt exactly on elements of:
   $$H = \Big\{\big\langle M\big\rangle\ M\ |\ M\ \text{doesn't halt on } \langle M\rangle\Big\}$$
   