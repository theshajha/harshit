# 01 — Variables & Data Types

> One line: a variable is just a name pointing at a value — and every value has a *type* that decides what you can do with it.

## The idea
A variable is a **label you stick on a value**: `age = 19` means "the name `age` now points to the value `19`." You don't declare types in Python (it's *dynamically typed*) — but every value still *has* a type, and the type controls what operations are legal. `"5" + "5"` is `"55"` (string join); `5 + 5` is `10` (math). Same symbol, different behavior, because the types differ.

The deepest thing to internalise early: **some types are immutable (can't be changed in place), some are mutable.** It explains a whole class of "why did my variable change?!" bugs later.

## Quick reference

```python
age = 19                 # int
price = 4.5              # float
name = "Harshit"         # str
is_student = True        # bool  (True / False — capitalised)
nothing = None           # the "no value" value

type(age)                # <class 'int'>  — ask any value its type

# converting between types
int("42")    -> 42
str(42)      -> "42"
float("3.1") -> 3.1
int(3.9)     -> 3        # truncates, doesn't round

# f-strings: the way to build text with values inside
f"{name} is {age}"       # 'Harshit is 19'

# multiple assignment
x, y = 1, 2
```

| Type | Example | Mutable? |
|------|---------|----------|
| `int` | `19` | n/a (immutable) |
| `float` | `4.5` | immutable |
| `str` | `"hi"` | **immutable** |
| `bool` | `True` | immutable |
| `None` | `None` | — |
| `list`, `dict`, `set` | see note 06 | **mutable** |

## Worked example

```python
subtotal = 250          # int
tax_rate = 0.18         # float
tax = subtotal * tax_rate          # 45.0  -> int * float = float
total = subtotal + tax             # 295.0
print(f"Total: ₹{total:.2f}")      # 'Total: ₹295.00'  (:.2f = 2 decimal places)
```

## Gotchas
- **`"5"` is not `5`.** Input from `input()` is always a string — convert with `int()`/`float()` before doing math, or `"5" * 2` gives `"55"`, not `10`.
- **`==` vs `is`:** `==` asks "same value?", `is` asks "literally the same object?". Use `==` for comparisons; reserve `is` for `is None`.
- **`/` always gives a float:** `6 / 2` is `3.0`, not `3`. Use `//` for whole-number division.
- **Immutability:** you can't change a string in place — `s[0] = "X"` errors. You make a *new* string instead.

## ✍️ Your turn
*After CS50P Week 0–1:*
- In your own words, what does "dynamically typed" mean, and why does `int(input(...))` matter?
- One example you wrote:

## Go deeper
- Real Python — Variables → <https://realpython.com/python-variables/>
