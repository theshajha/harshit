# 07 — Functions

> One line: a named, reusable block of code — the single most important tool for keeping programs understandable.

## The idea
A function packages some work behind a name so you can reuse it and read your program as a story instead of a wall of steps. It takes **inputs** (parameters), does something, and usually **returns** a result. Good functions do *one* thing and have a clear name. This is the first real step from "scripting" to "engineering."

## Quick reference

```python
def greet(name):                 # 'name' is a parameter
    return f"Hello, {name}"

greet("Harshit")                 # call it -> 'Hello, Harshit'

# default values
def power(base, exp=2):
    return base ** exp
power(5)        # 25   (exp defaults to 2)
power(5, 3)     # 125

# multiple return values (really a tuple)
def min_max(nums):
    return min(nums), max(nums)
lo, hi = min_max([3, 1, 9])      # 1, 9

# a function with no return gives back None
```

## Worked example
*(complete after the lecture)*
```python
def is_even(n):
    return n % 2 == 0
```

## Gotchas
- **`print` vs `return`** are different: `print` shows text to the user; `return` hands a value back to the code. A function that prints but doesn't return gives `None`.
- **Scope:** variables made inside a function don't exist outside it.
- Don't use a mutable default like `def f(x=[])` — it's a known trap (the list is shared across calls).

## ✍️ Your turn
- `print` vs `return`, in your own words:
- One function you wrote:

## Go deeper
- CS50P — Functions (Week 0/3)
