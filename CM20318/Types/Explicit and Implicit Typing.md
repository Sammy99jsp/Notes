## Dynamic Languages
In some languages (such as Python), you don't need to declare variables before you use them/assign to them.

```python
fruit = ["Apples", "Oranges"]
print(friut) ## <-- Oh no, runtime exception.
```
Likewise, in dynamic languages, you don't need to explicitly declare types.

Though, sometimes you can optionally add types to dynamic languages:
```python
# Python
def count(upper_bound: int) -> None:
	pass # Implementation skipped.
```

Though, in the case of Python, the runtime throws the type information away  
## Statically-Typed Languages
There are many different approaches that statically-typed languages can ascribe types to values.
### Explicit (Manifest) Typing
You must explicitly declare the types of things.
```c
// C
char fruit[] = "Apples";
```
### Implicit Typing
The compiler *infers* the type by itself based on the context.
```haskell
-- HASKELL
-- The compiler knows this is (Num a) => a -> a
inc = (+1)
```

Sometimes, languages do both:
```rust
// RUST
// In Rust, functions must have type annotations.
fn len_of(fruit: &[&'static str]) -> usize {
    fruit.len()
}

// Though, here, Rust will know the type of this.
let len_of_fruit = len_of(&["Apples", "Oranges"]);
```
In Rust, most places don't need explicit type annotations, barring some circumstances such as function signatures (or when `rustc` cannot figure it out*) — this choice was made by Rust's design team:
```rust
// By the way, this doesn't compile.
fn triple<Num>(x: Num) -> Num
	where Num: std::ops::Mul<usize, Output = Num>
{
	x * 3
}

// Somewhere else:

fn triple<Num>(x: Num) -> (Num, Num, Num)
	where Num: Copy
{
	(x, x, x)
}
```
\*Example:
![[RustTypeUnInference.png]]
### Comparison
Sometimes, leaving types out makes it harder to read the code later; sometimes, it makes it harder to understand (types can get unwieldy long).

