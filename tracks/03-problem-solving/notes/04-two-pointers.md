# 04 — Two Pointers

> One line: use two indices moving through an array — often from both ends — to avoid a nested loop.

## When to reach for it
Signals: the array is **sorted**, you need a **pair** that meets a condition, checking a **palindrome**, or doing something **in place**. Two pointers turn many O(n²) pair-search problems into O(n).

## The template
```python
# from both ends (e.g. find a pair summing to target in a SORTED array)
left, right = 0, len(arr) - 1
while left < right:
    total = arr[left] + arr[right]
    if total == target:
        return [left, right]
    elif total < target:
        left += 1        # need bigger -> move left up
    else:
        right -= 1       # need smaller -> move right down

# same direction (e.g. remove duplicates in place)
slow = 0
for fast in range(len(arr)):
    if arr[fast] != arr[slow]:
        slow += 1
        arr[slow] = arr[fast]
```

## Starter problems (solve these)
- [ ] Valid Palindrome
- [ ] Two Sum II (sorted input)
- [ ] 3Sum
- [ ] Container With Most Water

## Gotchas
- The "from both ends" trick usually needs the array **sorted** first.
- Watch your loop bound: `left < right` (not `<=`) when the two shouldn't overlap.

## ✍️ Your turn
- When two pointers beats a nested loop, in your words:
- A problem you solved with it:

## Go deeper
- NeetCode — Two Pointers
