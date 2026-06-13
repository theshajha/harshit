# 09 — Files & I/O

> One line: reading and writing files — how programs remember things between runs and work with real data.

## The idea
Programs forget everything when they stop — unless they write to a file. Python opens files with `open()`, and the `with` statement is the right way to do it because it **closes the file automatically**, even if something errors. For structured data, CSV and JSON are the two formats you'll meet first.

## Quick reference

```python
# read a whole file
with open("notes.txt") as f:
    text = f.read()

# read line by line (memory-friendly)
with open("notes.txt") as f:
    for line in f:
        print(line.strip())

# write (overwrites!) / append
with open("out.txt", "w") as f:    # "w" = write, "a" = append
    f.write("hello\n")

# CSV
import csv
with open("data.csv") as f:
    for row in csv.DictReader(f):   # each row is a dict by column name
        print(row["name"])

# JSON (great for structured data)
import json
data = json.loads('{"a": 1}')       # string -> dict
json.dumps({"a": 1})                # dict -> string
```

## Worked example
*(complete after the lecture)*
```python
with open("log.txt", "a") as f:
    f.write("ran today\n")
```

## Gotchas
- **`"w"` overwrites the whole file** — use `"a"` to add to it. Easy to wipe data by accident.
- Always use `with open(...)` — it closes the file for you. Forgetting to close causes subtle bugs.
- File paths are relative to where you *run* the script, not where the file lives.

## ✍️ Your turn
- The trickiest thing, in your words:
- One example you wrote:

## Go deeper
- CS50P — File I/O (Week 6)
