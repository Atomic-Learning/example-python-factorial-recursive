The calculation of the factorial of a number is a classic example of recursion because each factorial value can be defined using the factorial of a smaller number.

# Example implementation

```py-cell
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

print(factorial(0))
print(factorial(1))
print(factorial(6))
```

# How it works

The base case is `n`{.python} has the value 0, where a value of 1 is returned. For larger values, the function multiplies `n`{.python} by `factorial(n - 1)`{.python}, with the value of `n`{.python} passed to each subsequent call to the function decreased by 1 each time.

Eventually the call chain reaches `factorial(0)`{.python}, then returns values back up the chain to produce the final result.

# Practical Alternative

Whilst this approach will work well for small values of `n`{.python}, it can be inefficient for larger values due to the repeated calculations. When calcualting the factorial of a number in a real project, using `math.factorial()`{.python} (or `scipy.special.factorial()`{.python} for arrays of numbers) is more efficient and robust.
