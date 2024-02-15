Take a look at the factorial code:
```haskell
factorial :: Int -> Int
factorial 0 = 1
factorial n = n * (factorial (n-1))
```
In order to calculate `factorial 4`, a (dumb) compiler would have to do:
```haskell
factorial 4 = 4 * (factorial 3)                   -- (0)
			= 4 * (3 * (factorial 2))             -- (1)
			= 4 * (3 * (2 * (factorial 1)))       -- (2)
			= 4 * (3 * (2 * (1 * (factorial 0)))) -- (3)
			= 4 * (3 * (2 * (1 * 1)))             -- (4)
```
Notice, we have 5 expressions here on the stack, because each recursive step needs to know the result of the next.
For a large `n`, this leads to "space leaks" where the stacks use a lot of memory.

We can improve this by using an accumulator approach:
```haskell
accFactorial acc n
  | n <= 1    = acc
  | otherwise = accFactorial (acc * n) (n-1)

factorial' = accFactorial 1
```
Now, the evaluation looks a bit like this:
```haskell
factorial' 4    = accFactorial (1 * 4) 3          -- (0)
				= accFactorial (1 * 4 * 3) 2      -- (1)
				= accFactorial (1 * 4 * 3 * 2) 1  -- (2)
				= 1 * 4 * 3 * 2                   -- (3)
```

This is much easier on the computer since it can calculate the first element (the product) as-it-goes, which means its significantly more space efficient.

