# 01 — Big-O Notation (Complexity)

> One line: a way to describe how *slow* an algorithm gets as the input grows — so you can compare solutions without a stopwatch.

## The idea
Big-O answers: "if the input doubles, what happens to the work?" It ignores constants and small details and captures the *growth shape*. You don't need the math — you need to recognise a handful of common cases and spot them in your own code. The headline skill: **a nested loop over the same data is O(n²); replacing the inner lookup with a hash map (dict/set) makes it O(n).** That one move is most interview optimisations.

## Quick reference — from best to worst

| Big-O | Name | Looks like | Feel |
|-------|------|-----------|------|
| O(1) | constant | dict/set lookup, array index | instant |
| O(log n) | logarithmic | binary search (halving) | great |
| O(n) | linear | one loop through the data | fine |
| O(n log n) | linearithmic | good sorting | fine |
| O(n²) | quadratic | **nested loop** over the data | slow — avoid if you can |
| O(2ⁿ) | exponential | trying every combination | only tiny inputs |

```python
# O(n) — one pass
for x in items: ...

# O(n²) — loop inside a loop  (the smell to watch for)
for a in items:
    for b in items: ...

# O(1) lookup — the fix
seen = set(items)
if x in seen: ...        # instant, vs scanning the list (O(n))
```

## Worked example
*(complete after the concept clicks)*
- Brute-force Two Sum (nested loops) = **O(n²)**.
- Hash-map Two Sum (one pass + dict lookups) = **O(n)**.
- Same answer, hugely different speed at scale.

## Gotchas
- Big-O is about **growth**, not exact time — O(n) isn't always faster than O(n²) for *tiny* inputs, but it wins as data grows.
- A `in` check on a **list** is O(n); on a **set/dict** it's O(1). Choosing the right container *is* optimisation (see note 06 in the Python track).
- Nested loops aren't always O(n²) — only if both run over the input size.

## ✍️ Your turn
- Explain O(n) vs O(n²) in your own words:
- A solution where you cut O(n²) → O(n) with a set/dict:

## Go deeper
- Big-O cheat sheet → <https://www.bigocheatsheet.com>
