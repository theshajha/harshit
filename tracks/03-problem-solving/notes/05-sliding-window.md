# 05 — Sliding Window

> One line: keep a moving "window" over a contiguous run of elements, growing and shrinking it instead of re-scanning.

## When to reach for it
Signals: "longest/shortest **substring** or **subarray**", "**contiguous**", "at most K of something". Instead of checking every sub-range (O(n²)), you slide one window across in O(n).

## The template
```python
# longest window satisfying some condition
left = 0
best = 0
window = {}                      # or a running sum / count
for right in range(len(s)):
    # 1. add s[right] to the window
    window[s[right]] = window.get(s[right], 0) + 1

    # 2. shrink from the left while the window is invalid
    while not_valid(window):
        window[s[left]] -= 1
        left += 1

    # 3. record the best valid window
    best = max(best, right - left + 1)
return best
```

## Starter problems (solve these)
- [ ] Best Time to Buy and Sell Stock
- [ ] Longest Substring Without Repeating Characters
- [ ] Longest Repeating Character Replacement

## Gotchas
- The pattern is: **expand right, shrink left when invalid, record the best.** Get that rhythm and most window problems fall.
- Be clear whether you want the *longest* or *shortest* window — it changes where you record the answer.

## ✍️ Your turn
- The expand/shrink rhythm in your own words:
- A window problem you solved:

## Go deeper
- NeetCode — Sliding Window
