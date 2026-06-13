# 00 — How Python Runs & Your Setup

> One line: before any syntax, understand *what actually happens* when you run Python — it saves you hours of confusion later.

## The idea
Python is an **interpreter**: it reads your code top to bottom and runs it line by line. There's no separate "compile" step you manage (unlike C++ or Java). You write code two ways:
- **A script** — a `.py` file you run start-to-finish.
- **The REPL** — an interactive prompt where you type one line and see the result instantly. Great for trying things.

A **virtual environment** is a clean, per-project box for the libraries a project uses, so projects don't fight over versions. Make one per project — it's a habit, not a chore.

## Quick reference

```bash
python3 --version          # check Python is installed (use python3 on Mac/Linux)
python3 hello.py           # run a script
python3                    # start the REPL (Ctrl-D or exit() to leave)

# virtual environment (do this once per project)
python3 -m venv .venv      # create it
source .venv/bin/activate  # turn it on (Mac/Linux)   →  .venv\Scripts\activate on Windows
pip install requests       # install a library (only affects this project)
pip freeze > requirements.txt   # save your project's dependency list
deactivate                 # turn it off
```

| Tool | What it's for |
|------|---------------|
| **VS Code** + Python extension | where you write and run code |
| **python3** | runs your code |
| **pip** | installs libraries |
| **venv** | isolates each project's libraries |

## Worked example

```python
# hello.py
name = input("What's your name? ")
print(f"Hello, {name}!")
```

```bash
python3 hello.py
# What's your name? Harshit
# Hello, Harshit!
```

The file runs top to bottom: line 2 pauses for input, line 3 prints. That's it — no build, no main() required.

## Gotchas
- On Mac/Linux it's usually `python3`, not `python`. If `python` runs Python 2, you'll get weird errors — use `python3`.
- **Indentation is part of the language.** A stray space or tab can break a program (more on this in control flow).
- Forgetting to **activate** the venv → `pip install` puts the library in the wrong place. If imports "aren't found," check your venv is on (your prompt usually shows `(.venv)`).

## ✍️ Your turn
*After CS50P Week 0:*
- In your own words, what's the difference between the REPL and running a script?
- One example you wrote:

## Go deeper
- CS50P — Week 0 → <https://cs50.harvard.edu/python>
- The official Python tutorial, §1–2 → <https://docs.python.org/3/tutorial/>
