# 12 — Pythonic Idioms & Comprehensions

> One line: the shorter, clearer ways Python folks actually write things — the stuff that makes code look "Pythonic."

## The idea
Once the basics click, there's a set of idioms that make Python concise and readable. The headline one is the **comprehension** — building a list/dict/set in a single expressive line instead of a loop. Learn these and your code shrinks and reads better. (Clarity first, though — never make it cryptic to save a line.)

## Quick reference

```python
# list comprehension:  [ expression for item in iterable if condition ]
squares = [n*n for n in range(5)]            # [0, 1, 4, 9, 16]
evens   = [n for n in range(10) if n % 2 == 0]

# dict comprehension
lengths = {w: len(w) for w in ["hi", "bye"]} # {'hi': 2, 'bye': 3}

# set comprehension
unique_lens = {len(w) for w in words}

# handy idioms
", ".join(items)                 # list -> string
for i, x in enumerate(items): ...# index + value
for a, b in zip(list1, list2):...# walk two lists together
total = sum(nums); n = len(nums)
any(x > 0 for x in nums); all(...)   # quick checks
x = a if cond else b             # ternary
```

## Worked example
*(complete after you're comfortable with loops)*
```python
names = ["harshit", "rex"]
caps = [n.capitalize() for n in names]   # ['Harshit', 'Rex']
```

## Gotchas
- A comprehension should stay **readable**. If it needs two conditions and a nested loop, a plain `for` loop is clearer — write that instead.
- Comprehensions build a *new* collection; they don't modify in place.

## ✍️ Your turn
- Rewrite one of your earlier `for` loops as a comprehension and paste both:
- The idiom you find most useful:

## Go deeper
- Real Python — Comprehensions → <https://realpython.com/list-comprehension-python/>
