Types are seen as an aid to the programmer to help know *what* things actually are.
### Classes
Some languages have classes (which may, or may not be, types).
Java has primitive types (`int`, `char`), but also classes (`Integer`, `Character`).
C doesn't have classes, but has types.
Modern languages don't distinguish.
## Type Checking
### Static Typing
*Examples*: C, C++, Java, Haskell
Static type checking is where the compiler keeps track of the types of values (variables, expressions, function signatures).

The types can be thought of as "attached to the variables".

Static typing is common in modern languages.
### Dynamic Typing
Here, types are checked at runtime.

This can be thought of types "being attached to the values themselves" — the values have metadata that describe which type they are.

Dynamic typing is common in scripting languages.
### "Strong" typing
A value has a definite type, and no *implicit* conversion between types.
- Expressions are checked for type correctness at compile/run-time
- Little (or none) automatic type conversion (e.g. `int` -> `float`).

For example, Rust is more strongly typed than JavaScript.
### Weak typing
Languages that change the type where it sees fit.

Here, JavaScript thinks that `1 + "1" == "11"` — it coerces the number `1` to the string `"1"`.

 In general, some languages want to be "helpful" — this can be helpful sometimes, but also a hindrance other times, and cause bugs sometimes.
### Casting vs Coercion
"Casting" is usually the explicit conversion of a type, such as:
- `(float)1` (C)
- `1 as f32` (Rust)

Some programmers don't trust the compiler, and are of the opinion that casts should be used instead of implicit conversion (coercion).
### Untyped Languages
Here, values have no explicit meaning — just bits and bytes. It's up to the programmer to determine what to do with the binary data.