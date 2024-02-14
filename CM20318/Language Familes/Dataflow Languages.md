*Purpose*: concurrent, or stream programming
*Examples*: SISAL, Strand, spreadsheets
*Features*: data-driven computation

Here, code can be written out-of-order:
```python
w = x + y
x = 9
z = 2
```

In this case, the language would define `x` and `z` first to then evaluate `w`, even if `w` comes first in the code. In this way, it behaves similarly to event-driven languages.

These languages can also lend to be parallelised, as they already calculate the dependencies.