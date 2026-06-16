# 06 — Stack

> One line: a last-in-first-out pile — perfect for matching, nesting, and "the most recent thing."

## When to reach for it
Signals: **matching/nesting** (brackets, tags), "**most recent**", undo, or "next greater element". A stack lets you remember things in reverse order and pop them off as you resolve them. In Python, a plain list *is* a stack.

## The template
```python
stack = []
stack.append(x)      # push
stack.pop()          # pop the most recent
stack[-1]            # peek at the top (check it's not empty first!)
not stack            # True if empty

# classic: valid parentheses
pairs = {")": "(", "]": "[", "}": "{"}
stack = []
for ch in s:
    if ch in pairs:                      # a closing bracket
        if not stack or stack.pop() != pairs[ch]:
            return False
    else:                                # an opening bracket
        stack.append(ch)
return not stack                         # valid only if nothing left over
```

## Starter problems (solve these)
- [ ] Valid Parentheses
- [ ] Min Stack
- [ ] Evaluate Reverse Polish Notation
- [ ] Daily Temperatures (next greater element)

## Gotchas
- **Peeking/popping an empty stack crashes** — always check `if stack:` first.
- "Nesting" or "matching" in a problem statement is the loudest signal for a stack.

## ✍️ Your turn
- What "LIFO" means and when it's useful, in your words:
- A stack problem you solved:

## Go deeper
- NeetCode — Stack
