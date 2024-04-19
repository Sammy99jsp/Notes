***NOTATION***: $M:\tau$ says that term $\color{TealBlue}M$ has type $\color{green}\tau$

## Typing Context
A context $\Gamma$ is a finite function which maps variables to types, which can be written as a list:
$$\Gamma = {\color{TealBlue}x_1} : {\color{green}\tau_1},\ {\color{TealBlue}x_2} : {\color{green}\tau_2},\ \dots,\  {\color{TealBlue}\tau_n} : {\color{green}\tau_n}$$
***NOTATION***: $\Gamma,\ {\color{TealBlue}x} : {\color{green}\tau}$ means that context $\Gamma$ is extended st. variable ${\color{TealBlue}x}$ has type ${\color{green}\tau}$.

## Typing Judgements
These are actually prepositions that a lambda term has a specific type 

***NOTATION***: $\Gamma \vdash {\color{TealBlue}M}:{\color{green}\tau}$ says that $\color{TealBlue}M$ has type $\color{green}\tau$ in context $\Gamma$: "*if* each variable $\color{TealBlue}x_i$ has type $\color{green}\tau_i$, *then* $\color{TealBlue}M$ has type $\color{green}\tau$".

We pronounce $\vdash$ "derives".