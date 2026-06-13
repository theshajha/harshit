# 10 — Modules, Packages & pip

> One line: don't write everything yourself — Python's standard library and the wider ecosystem already solved most problems.

## The idea
A **module** is just a `.py` file of reusable code; a **package** is a folder of modules. Python ships with a huge **standard library** ("batteries included"), and for everything else there's **pip**, which installs third-party packages from PyPI. Knowing what already exists is a real skill — it's the difference between 3 lines and 300.

## Quick reference

```python
# use the standard library
import random
random.randint(1, 6)         # dice roll
import datetime
datetime.date.today()

from math import sqrt        # import just what you need
sqrt(16)                     # 4.0

# your own module: a file utils.py with a function clean()
from utils import clean
```

```bash
# install third-party packages (inside your venv!)
pip install requests
pip list                     # what's installed
pip freeze > requirements.txt        # save the list
pip install -r requirements.txt      # recreate it elsewhere
```

Useful standard-library modules to know exist: `random`, `datetime`, `math`, `os`, `sys`, `json`, `csv`, `re`, `collections`.

## Worked example
*(complete after the lecture)*
```python
import random
print(random.choice(["heads", "tails"]))
```

## Gotchas
- **Install inside your activated venv** (note 00), not globally — keeps projects clean.
- Don't name your file the same as a library you import (e.g. `random.py`) — Python imports *your* file by mistake.
- Pin versions in `requirements.txt` so your project still works later.

## ✍️ Your turn
- The trickiest thing, in your words:
- One module you used and what for:

## Go deeper
- CS50P — Libraries (Week 4) · Python Module Index → <https://docs.python.org/3/py-modindex.html>
