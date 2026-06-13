# 02 — Strings

> One line: text. You'll manipulate strings constantly — cleaning input, building output, parsing data.

## The idea
A string is a sequence of characters. It's **immutable** — every "change" actually makes a *new* string. You can index and slice it like a list, and there's a rich set of built-in methods for the common jobs (case, trimming, searching, splitting, joining).

## Quick reference

```python
s = "Hello, World"

len(s)              # 12
s[0]                # 'H'        (index from 0)
s[-1]               # 'd'        (last char)
s[0:5]              # 'Hello'    (slice: start:stop, stop excluded)
s.lower()           # 'hello, world'
s.upper()           # 'HELLO, WORLD'
s.strip()           # trims whitespace from both ends
s.replace("l","L")  # 'HeLLo, WorLd'
s.split(", ")       # ['Hello', 'World']   -> a list
", ".join(["a","b"])# 'a, b'               (list -> string)
s.startswith("He")  # True
"World" in s        # True   (substring check)
f"{s}!"             # f-strings to build text
```

## Worked example
*(seeded lightly — complete it after the lecture)*
```python
# clean and normalise a user's name
name = "  hArShIt  "
clean = name.strip().capitalize()   # 'Harshit'
```

## Gotchas
- Strings are **immutable**: `s[0] = "X"` errors. Build a new string instead.
- `split()` with no argument splits on any whitespace — handy for words.
- *(add your own as you hit them)*

## ✍️ Your turn
- The trickiest string thing you learned, in your words:
- One example you wrote:

## Go deeper
- Python docs — String methods → <https://docs.python.org/3/library/stdtypes.html#string-methods>
