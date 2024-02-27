## Monomorphic/Lexical Types
This is types as you'd usually think: these are concrete types such as `int` in C, or `String` in Java.
### Polymorphic Types
Polymorphic types can be more than one type (with optional boundaries) — this is shown by the use of **type variables**:
```haskell
-- Haskell
myFunc :: (Num a) => a -> a -- `a` can be any number here.
myFunc x = x * 2 
```
```rust
// Rust
fn make_two_of<C: Clone>(thing: C) -> (C, C) {
	(thing.clone(), thing)
}
```

