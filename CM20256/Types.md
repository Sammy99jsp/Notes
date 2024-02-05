
| Type | Example Values |
| ---- | ---- |
| `Bool` | `True`, `False` |
| `Integer` | Any integer (infinite precision). |
| `Int` | At least `[-2^29 .. 2^29-1]`, but depends. |
| `Float`, `Double` | `0.1`, `0.2e5`, `0.002`, `-0.3` |
| `Char` | `'a'`, `'b'`, `'f'` |
| `String` | `"apples"` — Secretly `[Char]`  |
### Functions are types, too!
Syntax: `a -> b`
### Type-annotations
You can manually assign variables/functions values types using the syntax:
```haskell
numberOfApples :: Int
numberOfApples = 2

squareMe :: Integer -> Integer
squareMe x = x * x
```