Lists are denoted `[a]` for type `a`, they are also defined inductively:
```haskell
data List a
  | []
  | a : (List a)
```