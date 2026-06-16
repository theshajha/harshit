# 01 — HTML: Structure & Semantics

> One line: HTML marks up *what things are* — a heading, a paragraph, a list, a link — using tags.

## The idea
HTML is content wrapped in **tags** that say what each piece *is*. Most tags come in pairs: `<p>...</p>` wraps a paragraph. Tags **nest** inside each other to form a tree. Use **semantic** tags (ones that describe meaning, like `<nav>`, `<header>`, `<button>`) over generic `<div>`s where you can — it's clearer, and better for accessibility and search engines.

## Quick reference

```html
<h1>…</h1> … <h6>      <!-- headings, h1 = biggest/most important -->
<p>…</p>               <!-- paragraph -->
<a href="https://…">link</a>      <!-- link -->
<img src="me.jpg" alt="description">   <!-- image (alt = text if it fails) -->
<ul><li>item</li></ul>            <!-- bullet list -->
<ol><li>item</li></ol>            <!-- numbered list -->
<button>Click</button>

<!-- structure / semantic containers -->
<header> <nav> <main> <section> <footer>
<div>     <!-- generic box, when nothing semantic fits -->
<span>    <!-- generic inline wrapper -->

<!-- attributes give tags extra info -->
<a href="..." target="_blank">   <!-- href, target are attributes -->
<img src="..." alt="...">
```

Page skeleton every file starts with:
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Title in the browser tab</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <!-- everything you SEE goes here -->
  </body>
</html>
```

## Worked example
```html
<main>
  <h1>Harshit Jha</h1>
  <p>CS student. I build things.</p>
  <a href="https://github.com/...">My GitHub</a>
</main>
```

## Gotchas
- **Always add `alt` to images** — it's read aloud to blind users and shows if the image fails.
- `<head>` is metadata (not shown); `<body>` is what's visible. New people often put content in the wrong one.
- Indentation doesn't matter to the browser, but keep it tidy so *you* can read the nesting.

## ✍️ Your turn
- What does "semantic HTML" mean, in your words?
- Paste a small page you marked up:

## Go deeper
- MDN — HTML basics → <https://developer.mozilla.org/en-US/docs/Learn/HTML>
