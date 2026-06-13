# 04 — Control Flow (if / elif / else)

> One line: how your program *decides* — running different code depending on conditions.

## The idea
`if` runs a block only when a condition is `True`. `elif` ("else if") checks more conditions; `else` catches everything left. Python uses **indentation** (not braces) to mark what's "inside" the block — so indentation is real syntax here, not just style.

## Quick reference

```python
if score >= 90:
    grade = "A"
elif score >= 80:        # checked only if the first was False
    grade = "B"
else:
    grade = "C"

# comparisons
==  !=  <  >  <=  >=

# combine conditions
if age >= 18 and is_citizen:  ...
if a or b:  ...
if not done:  ...

# truthiness: these are all "falsy"
0, 0.0, "", [], {}, None, False     # everything else is "truthy"

# ternary (one-line if)
status = "adult" if age >= 18 else "minor"
```

## Worked example
*(complete after the lecture)*
```python
temp = 31
if temp > 30:
    print("hot")
elif temp > 20:
    print("pleasant")
else:
    print("cold")
```

## Gotchas
- **Indentation matters** — mixing tabs and spaces, or wrong indent level, changes meaning or errors. Pick spaces (4) and stay consistent (VS Code does this for you).
- `=` (assign) vs `==` (compare) — a classic bug.
- You rarely need `if x == True:` — just write `if x:`.

## ✍️ Your turn
- The trickiest thing, in your words:
- One example you wrote:

## Go deeper
- CS50P — Conditionals (Week 1)
