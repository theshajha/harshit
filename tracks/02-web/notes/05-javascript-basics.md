# 05 — JavaScript: The Basics

> One line: the language that makes pages *do* things — and your second programming language after Python.

## The idea
JavaScript adds behaviour to a page. The good news: you already know how to program from Python, so this is mostly learning new syntax for the same ideas (variables, functions, conditionals, loops, arrays, objects). The differences worth noting: `let`/`const` instead of bare names, curly braces `{ }` instead of indentation, and `===` for comparison.

## Quick reference

```javascript
// variables — use const by default, let if it changes
const name = "Harshit";
let count = 0;

// types: number, string, boolean, null, undefined, object, array
const nums = [1, 2, 3];                 // array  (like a Python list)
const user = { name: "H", age: 19 };    // object (like a Python dict)

// functions
function greet(name) { return `Hi, ${name}`; }   // template literals use backticks
const square = (n) => n * n;                       // arrow function

// conditionals & loops
if (count === 0) { ... } else { ... }    // === not ==
for (const n of nums) { console.log(n); }
nums.forEach(n => console.log(n));

console.log("debug here");               // prints to the browser console (F12)
```

| Python | JavaScript |
|--------|-----------|
| `True / False / None` | `true / false / null` |
| `elif` | `else if` |
| `#` comment | `//` comment |
| `len(x)` | `x.length` |
| f-string `f"{x}"` | template `` `${x}` `` |

## Worked example
*(complete after you try it)*
```javascript
const double = (n) => n * 2;
console.log(double(5));   // 10
```

## Gotchas
- Use **`===`** (strict equals), not `==` — `==` does weird type coercion (`0 == ""` is true). Just always use `===`.
- `const` doesn't mean frozen — you can still change *inside* an array/object, you just can't reassign the name.
- Open the **browser console (F12)** to see `console.log` output and errors.

## ✍️ Your turn
- Two differences between Python and JavaScript you noticed:
- Paste a small JS snippet you wrote:

## Go deeper
- MDN — JavaScript first steps → <https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps>
