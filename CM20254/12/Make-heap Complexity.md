Since we need to sift down, let's look at how long that takes:

| Level | Nodes | Steps per node |
|---|--|--|
| Lowest | $2^n$ | 0 |
| Penultimate | $2^{n-1}$| 1|
| Pen-penultimate | $2^{n-2}$ | 2 |
| Pen-pen-penultimate | $2^{n-3}$ | 3|
| ... | ...|
| First | $1$ | n |

So, for a tree with $n$ levels, the maximum number of steps make is:
$$2^n \times 0 + 2^{n-1} \times 1 + 2^{n-2} \times 2 + \dots + 2^1 \times(n-1) + 1 \times n = 2^n \sum_{k=1}^n \frac{k}{2^k}$$

It is proven that:
$$\sum_{k=1}^n \frac{k}{2^k} < \sum_{k=1}^\infty \frac{k}{2^k} = 2$$
Therefore, the total number of steps $\leq 2 \times 2^n = 2^{n+1}$
As the total number of nodes in the $n$-deep tree is $2^{n-1} - 1$, therefore make-heap has $O(n)$ complexity. 