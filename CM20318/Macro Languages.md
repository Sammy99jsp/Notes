*Purpose*: to improve readability of other code, abstraction, text manipulation.
*Examples*: C Pre-Processor, LATEX, M4, Lisp macors
*Features*: Lexical (character/text-based) manipulation, with some exceptions that are syntax-based (Lisp, Rust).

Typically macros are run at compile-time, essentially looking for code and replacing it before it's compiled.

These are very useful for a lot of contexts, such as conditional compilation (such as optional features, or different architectures) — write code once that can target different circumstances.

### Example: C Pre-Processing Language
CPP works on mainly a lexical basis (as in, it doesn't understand the syntax of the language).

```c
#include <stdio.h>

#ifdef FRUITS
#define APPLES 10
#ifndef FRUITS
#define APPLES 0
#endif

int main(char* argv[], int argc) {
  printf("I have %d apples!", APPLES);
}
```
### Example: Rust
Rust has syntax-based macros — these can only manipulate and output valid syntax, not text (or technically lexical tokens).
