## Lists
Lists are homogeneously-typed (same type) and are represented `List a` (where `a` is the type of the elements).

Lists are defined like so:
```haskell
List a
	| [] -- Empty list
	-- head :: a (start, here because `head` is a global function),
	-- then the rest of the list rest :: [a]
	| start : rest
```
Notice the `:` operator — the "cons" or constructor operator, it makes a construction 