Parallelism is the concept of doing multiple things at once — however, most programming languages are not explicitly designed for parallelism.

Some languages are naturally more adept to parallelism:
- Declarative languages — the implementation can do whatever it wants, which means it can be parallelised.
- Functional languages — the strict input -> output without any side effects means multiple threads don't interfere with each other.

Most sequential languages used have tried to introduce parallelism, with various levels of safeguarding:
- For example, C code will let you have shared state between threads that can be modified by any of them — no safeguards or synchronisation out of the box; you'll need to do that yourself!
- Rust has in-built safety to ensure that things are synchronised.


## Specifically Designed Parallel Languages
- Occam (1993) — derived from a mathematical notation for parallel processes.
- Strand — declarative, derived from Prolog.
- Erlang — functional. Used in real applications.
- Go — designed to replace C.
- Rust — designed from the start to be memory-safe.

Most parallel code is written in C, C++, or Java with some extra libraries — though, it is easier (but not necessarily practical, or cost-effective) to write it in a new language. 