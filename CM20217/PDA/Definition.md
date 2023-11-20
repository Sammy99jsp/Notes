## Definition: Pushdown Automata
A pushdown automaton (PDA) consists of six objects $\big(Q,\ \Sigma,\ \Gamma,\ s,\ \Delta,\ F\big)$, where:

Symbol | Definition
-- | --
$Q$ | finite set of **states**
$\Sigma$ | the **input alphabet**
$\Gamma$ | the **stack alphabet**
$s \in Q$ | **initial state**
$F \subseteq Q$ | **accepting states**
$\Delta \subseteq \big(Q \times (\Sigma \cup \{e\}) \times \Gamma^\ast\big) \times \big(Q \times \Gamma^\ast\big)$ | **transition relation**

Unfortunately, there are many different definitions of pushdown automata (which are ultimately equivalent).
### $\Gamma$ - The stack alphabet
$\Gamma$ represents all possible things that can be members of the stack.
It's important to realise that elements of the stack are words, such as $00010$.

Therefore, $\Gamma^\ast$ represents all possible configurations of the stack.
### $\Delta$ Transitions in PDAs
Let's look at what the $\Delta$ represents - here's what a member of that set looks like:
$$\big((p,\ a,\ \alpha),\ (q,\ \beta)\big)$$
The above tuple of tuples represents an individual transition arrow on a diagram, it represents:
* We're at state $p$ with (potentially empty), reading input $a$, with $\alpha$ at the top of the stack - $\alpha$ is always popped off the top of the stack*
* Then, moving to state $q$, and pushing $\beta$ to the top of the stack*.

\***Notice** that it is compulsory to interact with the stack - we must pop $\alpha$ in order to move to state $q$; just like we must push $\beta$ to the top of the stack. If we don't want to pop/push something, we can put an empty word $e$ in the appropriate place instead.
