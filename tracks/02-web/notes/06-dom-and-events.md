# 06 — The DOM & Events

> One line: how JavaScript *reaches into the page* to change it and respond to clicks — where a site becomes interactive.

## The idea
The browser turns your HTML into a live tree of objects called the **DOM** (Document Object Model). JavaScript can grab elements from that tree and change them — text, styles, anything — and it can **listen for events** (clicks, typing, submits) and run code in response. "Find an element → do something to it, when something happens" is the whole game of interactive pages.

## Quick reference

```javascript
// 1. grab an element
const btn = document.querySelector("#myButton");   // CSS selector
const title = document.querySelector("h1");

// 2. change it
title.textContent = "New heading";
title.style.color = "crimson";
title.classList.toggle("dark");        // add/remove a CSS class

// 3. respond to events
btn.addEventListener("click", () => {
  console.log("clicked!");
});

// reading input
const input = document.querySelector("#name");
input.value;                            // what the user typed
```

Common events: `click`, `input`, `submit`, `keydown`, `mouseover`.

## Worked example
*(complete after you try it — a dark-mode toggle is a perfect first one)*
```javascript
const toggle = document.querySelector("#themeBtn");
toggle.addEventListener("click", () => {
  document.body.classList.toggle("dark");
});
```

## Gotchas
- Run your JS **after** the HTML exists — put `<script src="script.js">` at the **end of `<body>`**, or the elements won't be found yet (`null`).
- `textContent` (safe, plain text) vs `innerHTML` (parses HTML — avoid with user input; it's a security risk).

## ✍️ Your turn
- In your words, what is "the DOM"?
- Paste an interactive thing you built (e.g. your toggle):

## Go deeper
- MDN — Introduction to the DOM → <https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction>
