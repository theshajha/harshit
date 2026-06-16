# 03 — Arrays & Hashing

> One line: the workhorse pattern — use a hash map (dict) or set to remember things and look them up instantly.

## When to reach for it
Signals: "have I seen this before?", counting occurrences, removing duplicates, "find two things that relate." Anytime a brute force does repeated *searching*, a dict/set usually turns O(n²) into O(n).

## The tool & template
```python
# set  -> fast membership / dedupe
seen = set()
for x in items:
    if x in seen:        # O(1) lookup
        ...              # found a duplicate
    seen.add(x)

# dict -> count things, or map value -> index
counts = {}
for x in items:
    counts[x] = counts.get(x, 0) + 1     # frequency count

# dict -> remember where you saw something (Two Sum style)
index_of = {}
for i, x in enumerate(items):
    if target - x in index_of:
        return [index_of[target - x], i]
    index_of[x] = i
```

## Starter problems (solve these)
- [ ] Contains Duplicate
- [ ] Two Sum
- [ ] Valid Anagram
- [ ] Group Anagrams

## Gotchas
- `dict[key]` crashes on a missing key — use `.get(key, default)`.
- A set lookup is O(1); the same `in` check on a list is O(n). The container choice *is* the optimisation.

## ✍️ Your turn
- The signal that tells you "this is a hashing problem", in your words:
- A problem you solved with a dict/set (paste it):

## Go deeper
- NeetCode — Arrays & Hashing
