# 03 — Numbers & Math

> One line: ints, floats, and the operators — plus the two division traps everyone hits once.

## The idea
Two main number types: **`int`** (whole) and **`float`** (decimal). Mixing them gives a float. Most operators are obvious; the ones worth memorising are integer division `//`, modulo `%` (remainder), and power `**`.

## Quick reference

```python
7 + 2      # 9
7 - 2      # 5
7 * 2      # 14
7 / 2      # 3.5     <- always a float
7 // 2     # 3       <- integer (floor) division
7 % 2      # 1       <- remainder (great for "is even?", cycling)
7 ** 2     # 49      <- power

round(3.14159, 2)   # 3.14
abs(-5)             # 5
min(3, 9), max(3, 9)# (3, 9)

import math
math.sqrt(16)       # 4.0
math.floor(3.9)     # 3
```

## Worked example
*(complete after the lecture)*
```python
# is a number even?
n = 10
is_even = (n % 2 == 0)   # True
```

## Gotchas
- `/` is **always** a float (`6 / 2` → `3.0`). Use `//` when you want a whole number.
- `%` (modulo) is your friend for "every Nth", even/odd, wrapping around a range.
- Floats are slightly imprecise (`0.1 + 0.2 != 0.3`) — fine for most things, avoid for money math.

## ✍️ Your turn
- The trickiest thing, in your words:
- One example you wrote:

## Go deeper
- Python docs — Numeric types → <https://docs.python.org/3/library/stdtypes.html#numeric-types-int-float-complex>
