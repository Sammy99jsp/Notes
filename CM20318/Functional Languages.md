*Purpose*: general programming, symbolic programming
*Examples*: Lisp, Scheme, Haskell, ML, Erlang, Scala, ...
*Features*:
- higher-order functions provide structure and control;
- avoidance of side-effects;
- immutability: avoidance of variable updates and value modification.

*First-class functions*: functions are values too — you can pass them as parameters, and return them too!

Data structures are treated as a whole thing, rather than by their elements — this is known as pointfree, tacit, or combinator programming.

```js
let vector = [3, 3, 3];

// Pointfree Programming
let incremented_vector = vector.map(x => x + 1); 

// The for-loop way
for (let i = 0; i < vector.length; i++)
  incremented_vector[i] += 1;
```
## Unpopular, but correct
- Functional languages may not be that popular, but their concepts and styles have bled into mainstream languages: such as closures, maps, and iterators — they can seem more "natural".
- Data immutability and maps can lead themselves to parallelism.