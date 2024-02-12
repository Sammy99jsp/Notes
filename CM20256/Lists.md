Lists are denoted `[a]` for type `a`, they are also defined inductively:
```haskell
data List a
  | Empty
  | NotEmpty a (List a)
```

Notice, lists are recursively defined: they are the `Cons` (construction) of a `head` and a `tail`