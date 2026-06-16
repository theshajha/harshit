# 00 — How to Solve Any Problem

> One line: the repeatable method that beats "staring and hoping" — the single most valuable thing in this track.

## The idea
Beginners freeze because they try to jump straight to the perfect solution. Strong problem-solvers follow a **process** instead. The trick isn't being clever — it's being *systematic*: understand it, work a small example by hand, get *any* working solution, then improve it. Slowness is fine; the method is what you're training.

## The method (use it every time)

```
1. UNDERSTAND   Read it twice. What are the inputs and outputs?
                Restate the problem in your own words.

2. EXAMPLES     Work one small example BY HAND, on paper.
                Try an edge case: empty input? one item? duplicates?

3. BRUTE FORCE  Get ANY correct solution, even a slow/ugly one.
                A working brute force beats a broken "clever" one.

4. OPTIMISE     Now ask: where's the waste? Can a hash map (note 03)
                or a pattern (note 02) remove a nested loop?

5. CODE         Write it. Small steps. Run it often.

6. TEST         Re-run your examples + the edge cases from step 2.
```

## Worked example (the method on "Two Sum")
> *Find two numbers in a list that add up to a target.*
1. **Understand:** in = list + target; out = the two indices.
2. **Examples:** `[2,7,11], target 9` → `[0,1]`. Edge: no answer? duplicates?
3. **Brute force:** two nested loops, check every pair. Works! (slow, O(n²))
4. **Optimise:** as you scan, remember numbers you've seen in a *dict*; for each number check if `target - n` is already seen → one pass, O(n).
5/6. Code it, test on the examples.

That jump from step 3 to step 4 — "a dict removes a loop" — is 80% of optimisation.

## Gotchas
- **Don't skip steps 1–2.** Most wrong answers are from not understanding the question, not from bad coding.
- A brute force on the board is a *win* — it shows you understand the problem and gives you something to improve.
- Talk/think out loud. In real interviews, your *reasoning* is what's graded, not just the final code.

## ✍️ Your turn
- The method in your own words (your version of the 6 steps):
- A problem where going brute-force-first unblocked you:

## Go deeper
- NeetCode — how to start → <https://neetcode.io>
