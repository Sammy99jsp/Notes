> Types were first proposed by Bertrand Russell in his development of mathematical logic.

In $\lambda$-calculus, every term is a function, so its type will determine:
* What input it expects
* What output it returns

We can define a simple grammar of types:
$$\tau ::= \omicron\ |\ \tau \rightarrow \tau $$
Where omicron $\omicron$ is called a *base type*, which could be something like `Int`, `Bool`, `Char`, etc (and even type functions, such as `[]`, or `IO`).

Notice that we can make a new type using an implication $(\tau \rightarrow \tau)$, (which will also represent the type of a function!).

### Examples
- $\omicron \rightarrow \omicron$
- $\omicron \rightarrow (\omicron \rightarrow \omicron)$ 
- $(\omicron \rightarrow \omicron) \rightarrow (\omicron \rightarrow \omicron)$

***NOTATION***: $\rightarrow$ is right-associative, meaning $\omicron \rightarrow (\omicron \rightarrow \omicron) \equiv \omicron \rightarrow \omicron \rightarrow \omicron$
