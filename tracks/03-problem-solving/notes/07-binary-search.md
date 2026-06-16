# 07 — Binary Search

> One line: find something in *sorted* data by repeatedly halving the search space — O(log n), absurdly fast.

## When to reach for it
Signals: data is **sorted** and you need to **find something fast**, or you're "**guessing a number**" and can tell if your guess is too high/low. Halving each step means even a million items take ~20 checks.

## The template
```python
def binary_search(arr, target):
    lo, hi = 0, len(arr) - 1
    while lo <= hi:
        mid = (lo + hi) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            lo = mid + 1        # target is in the right half
        else:
            hi = mid - 1        # target is in the left half
    return -1                   # not found
```

The same idea works on an *answer range* ("smallest X that works"), not just arrays.

## Starter problems (solve these)
- [ ] Binary Search
- [ ] Search a 2D Matrix
- [ ] Koko Eating Bananas (search on the answer)
- [ ] Find Minimum in Rotated Sorted Array

## Gotchas
- The data **must be sorted** (or you sort it first).
- The classic bugs are the boundaries: `lo <= hi`, and `mid + 1` / `mid - 1`. Get them right once and reuse the template.
- `(lo + hi) // 2` is fine in Python (no overflow) — in Java prefer `lo + (hi - lo) / 2`.

## ✍️ Your turn
- Why binary search is O(log n), in your words:
- A binary-search problem you solved:

## Go deeper
- NeetCode — Binary Search
