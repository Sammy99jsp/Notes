                                                                        ## Church Numerals
The standard way (there are others!) to represent natural numbers in $\lambda$-calculus is Church Numerals, which are of the form:
$$n \triangleq \lambda f. \lambda x. \underbrace{f(f(f(\dots (f(n)\dots)))}_{n\ \text{times}}$$
Which means that function $f$ is applied to $x$ $n$ times where $n \in \mathbb N$, so:
$$\begin{array}{ccl}&0 &\triangleq &\lambda f. \lambda x. x\\&1 &\triangleq & \lambda f. \lambda x. f\ x\\ & 2 &\triangleq &\lambda f.\lambda x. f \left(f\ x\right)\\&&\vdots&\end{array}$$
and so on.

### Successor
We can find the next natural number using the $\text{succ}$ function:
$$\text{succ} \triangleq \lambda n.\lambda f.\lambda x. f \left(n\ f\ x\right)$$