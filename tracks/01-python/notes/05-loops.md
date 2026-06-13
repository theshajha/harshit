# 05 — Loops (for / while)

> One line: how your program *repeats* — doing something for each item, or until a condition changes.

## The idea
A **`for`** loop walks through a sequence (a list, a string, a range) — "do this for each item." A **`while`** loop keeps going *until* a condition becomes `False` — "keep doing this while true." Reach for `for` when you know what you're iterating over; `while` when you're waiting for something to change.

## Quick reference

```python
# for: iterate over items
for item in [10, 20, 30]:
    print(item)

for ch in "hello":           # strings are iterable too
    print(ch)

for i in range(5):           # 0,1,2,3,4
    print(i)
for i in range(1, 11, 2):    # start, stop, step -> 1,3,5,7,9

# while: repeat until condition is False
n = 5
while n > 0:
    print(n)
    n -= 1                   # MUST change, or it loops forever

# loop controls
break        # exit the loop now
continue     # skip to the next iteration

# loop with index + value
for i, item in enumerate(["a", "b"]):   # 0 'a', 1 'b'
    print(i, item)
```

## Worked example
*(complete after the lecture)*
```python
total = 0
for n in [1, 2, 3, 4]:
    total += n          # 10
```

## Gotchas
- **Infinite `while`**: forget to change the condition variable and it never ends (Ctrl-C to stop). Always ask "what makes this loop end?"
- Use `range(len(x))` only when you truly need the index — usually `for item in x` (or `enumerate`) is cleaner.

## ✍️ Your turn
- The trickiest thing, in your words:
- One example you wrote:

## Go deeper
- CS50P — Loops (Week 2)
