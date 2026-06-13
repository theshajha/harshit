# 06 — Lists, Dicts, Sets, Tuples

> One line: the four containers you'll use every single day — and knowing *which* to reach for is half of writing good Python.

## The idea
Most programs are "do something to a bunch of things." Python gives you four built-in containers, and choosing the right one makes code clearer and faster. The decision comes down to three questions: **Ordered? Changeable? Duplicates allowed?**

| Container | Looks like | Ordered | Changeable | Duplicates | Reach for it when… |
|-----------|-----------|---------|-----------|------------|---------------------|
| **list** | `[1, 2, 3]` | yes | yes | yes | an ordered sequence you'll add to / change |
| **dict** | `{"a": 1}` | yes* | yes | keys unique | you look things up *by name/key* |
| **set** | `{1, 2, 3}` | no | yes | **no** | you need uniqueness / fast "is X in here?" |
| **tuple** | `(1, 2)` | yes | **no** | yes | a fixed group that shouldn't change |

\*dicts keep insertion order in modern Python.

## Quick reference

```python
# ---------- LIST ----------
nums = [3, 1, 2]
nums[0]            # 3            (index from 0)
nums[-1]           # 2            (last)
nums[0:2]          # [3, 1]       (slice)
nums.append(4)     # add to end
nums.remove(1)     # remove a value
nums.sort()        # sort in place
len(nums)          # count
3 in nums          # membership -> True

# ---------- DICT (key -> value) ----------
person = {"name": "Harshit", "age": 19}
person["name"]            # 'Harshit'
person.get("email")       # None  (safe — no crash if missing)
person["email"] = "h@x"   # add / update
for key, value in person.items():  ...   # loop both
person.keys(); person.values()

# ---------- SET (unique, unordered) ----------
seen = {1, 2, 2, 3}       # -> {1, 2, 3}  (dupes dropped)
seen.add(4)
2 in seen                 # very fast membership check
{1,2,3} & {2,3,4}         # intersection -> {2, 3}

# ---------- TUPLE (fixed) ----------
point = (4, 5)
x, y = point              # unpack
# point[0] = 9           # ERROR — tuples can't change
```

## Worked example

```python
# Count how many times each word appears — a classic dict job
text = "to be or not to be"
counts = {}
for word in text.split():            # split() -> list of words
    counts[word] = counts.get(word, 0) + 1
print(counts)   # {'to': 2, 'be': 2, 'or': 1, 'not': 1}
```

`counts.get(word, 0)` means "current count, or 0 if we haven't seen it" — the clean way to avoid a `KeyError`.

## Gotchas
- **`dict[key]` crashes if the key is missing** (`KeyError`). Use `.get(key)` (returns `None`) or `.get(key, default)` when unsure.
- **Aliasing:** `b = a` (for a list/dict) makes `b` point at the *same* list — changing `b` changes `a`. To copy, use `a.copy()` or `a[:]`.
- **Sets are unordered** — don't rely on the order things come out.
- Use a **tuple** (not a list) when something shouldn't change — it signals intent and can be a dict key.

## ✍️ Your turn
*After CS50P (loops + the relevant psets):*
- In your own words, when do you pick a dict over a list?
- One example you wrote (e.g. your own counting or lookup program):

## Go deeper
- Python docs — Data Structures → <https://docs.python.org/3/tutorial/datastructures.html>
