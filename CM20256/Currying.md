What if we want to implement, say multiplication?

In Haskell, functions can only have one parameter at a time — then how can we have multiple arguments?

We curry (named after Logician Haskell B. Curry)!
```haskell
multiply :: Integer -> (Integer -> Integer)
multiply x y = x * y
```

Notice, we can call multiply with one argument:
```haskell
doubleIt y = multiply 2
```
Now, we can call `doubleIt 7` to get `14`; or, more directly `multiply 2 7`.
### Function Evaluation
Function types are written left-to-right (where the right-most type is the output), so:
`Integer -> Integer -> Integer == Integer -> (Integer -> Integer)`
But not: `(Integer -> Integer) -> Integer`.

Functions are evaluated from right-to-left however:
`divide 7.0 2.0 == 3.5`.