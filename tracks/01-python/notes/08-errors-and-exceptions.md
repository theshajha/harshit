# 08 — Errors & Exceptions

> One line: things go wrong at runtime — exceptions are how Python tells you, and how you handle it gracefully instead of crashing.

## The idea
When Python can't do something (divide by zero, convert `"abc"` to an int, open a missing file), it **raises an exception** — and stops, printing a traceback. You can **catch** expected problems with `try`/`except` so the program responds sensibly instead of crashing. Read tracebacks bottom-up: the last line is *what* went wrong.

## Quick reference

```python
try:
    age = int(input("Age: "))
except ValueError:                 # runs only if that error happens
    print("Please enter a number")
else:
    print("Thanks!")               # runs if NO error
finally:
    print("done")                  # always runs

# common built-in exceptions
ValueError      # wrong value, e.g. int("abc")
TypeError       # wrong type, e.g. "a" + 1
KeyError        # missing dict key
IndexError      # list index out of range
FileNotFoundError
ZeroDivisionError

# raise your own
raise ValueError("score must be positive")
```

## Worked example
*(complete after the lecture)*
```python
def safe_div(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return None
```

## Gotchas
- **Catch specific exceptions**, not a bare `except:` — a blanket catch hides real bugs.
- Don't use exceptions for normal flow you can check for (e.g. use `dict.get()` rather than catching `KeyError`).
- **Read the traceback** — it names the file, line, and error type. That's a feature, not noise.

## ✍️ Your turn
- The trickiest thing, in your words:
- One example you wrote:

## Go deeper
- CS50P — Exceptions (Week 3)
