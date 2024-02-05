### Haskell is...
* Functional — *nearly* everything is a function (see [Currying]).
* Statically-typed — [Types] are enforced and checked at runtime.
* Lazy (evaluated) — expressions are evaluated only when needed.
## Examples
### (1) Factorial Function
```haskell
factorial :: Integer -> Integer
factorial x
  | x <= 1      = 1
  | otherwise x = x * factorial (x-1)
```
### (2) Hello World
```haskell
main :: IO ()
main = do
  print "Hello, world!"
```
## Guards
Guards are like `if`-statements, but multiple together, such as in (1).
**Note:** that `otherwise` is secretly just `True`, so it will always match.
## Recursion
Recursion is the entire point of a language like Haskell.