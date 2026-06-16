# 02 — The Pattern Catalog

> One line: ~90% of problems are variations of a small set of patterns — learn to *recognise which one* and you're halfway done.

## The idea
You don't memorise hundreds of problems; you learn a handful of **patterns** and the **signals** that tell you which to use. When you read a new problem, the real question is "which pattern is this?" This note is the map — each row links to its own note as you build them out. (This is also exactly how the NeetCode roadmap is organised.)

## The catalog — pattern → when to reach for it

| Pattern | Signal in the problem | Note |
|---------|----------------------|------|
| **Arrays & Hashing** | "have I seen this?", counting, dedupe, fast lookup | [03](03-arrays-and-hashing.md) |
| **Two Pointers** | sorted array, pair from both ends, in-place | [04](04-two-pointers.md) |
| **Sliding Window** | longest/shortest substring or subarray, "contiguous" | [05](05-sliding-window.md) |
| **Stack** | matching/nesting (brackets), "most recent", undo | [06](06-stack.md) |
| **Binary Search** | sorted data, "find X fast", or guessing a number | [07](07-binary-search.md) |
| Linked Lists | reverse/reorder nodes, fast/slow pointers | *(coming)* |
| Trees / BFS-DFS | hierarchy, levels, "all paths" | *(coming)* |
| Graphs | nodes + connections, grids, "reachable" | *(coming)* |
| Dynamic Programming | "number of ways", "min/max to…", overlapping subproblems | *(coming)* |

## How to use it
When stuck on a new problem, run down this list and ask "does the signal match?" Often the keyword in the prompt (*sorted*, *contiguous*, *most recent*, *number of ways*) points straight at the pattern.

## Gotchas
- Don't force a fancy pattern — if brute force is fast enough for the input size, it's a fine answer.
- Many hard problems are **two patterns combined** (e.g. sliding window + hashing). Learn each cleanly first.

## ✍️ Your turn
- Add the signal phrases *you* notice map to each pattern:
- The pattern you find hardest to recognise:

## Go deeper
- NeetCode Roadmap (this catalog, as a practice path) → <https://neetcode.io/roadmap>
