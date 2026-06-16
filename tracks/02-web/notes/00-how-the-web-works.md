# 00 — How the Web Works

> One line: before any tags, understand the three languages of the web and what each one is *for* — it makes everything after click.

## The idea
Every website is built from three languages, each with one job:
- **HTML** — the **structure** (headings, paragraphs, images, buttons). The skeleton.
- **CSS** — the **style** (colours, fonts, spacing, layout). The skin and clothes.
- **JavaScript** — the **behaviour** (clicks, changes, fetching data). The muscles.

When you visit a page, your **browser** downloads these files and *renders* them into what you see. That's it — a website is just text files the browser knows how to draw. You can build one with nothing but a text editor and a browser.

## Quick reference

```
A web page = HTML  (structure)
           + CSS   (style)
           + JS    (behaviour)

You write:        index.html, style.css, script.js
The browser:      downloads them, draws the page
To see your work: just open the .html file in a browser (double-click it)
```

| Language | Answers the question | File |
|----------|---------------------|------|
| HTML | *What's on the page?* | `.html` |
| CSS | *What does it look like?* | `.css` |
| JavaScript | *What does it do?* | `.js` |

## Worked example
The smallest possible web page — save as `index.html`, double-click to open:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Hello, web!</h1>
  </body>
</html>
```
You just made a website. No tools, no install — the browser did the rest.

## Gotchas
- You don't need a server or any install to start — opening an `.html` file works.
- Keep the three concerns separate: structure in HTML, looks in CSS, behaviour in JS. Mixing them is what makes pages a mess.

## ✍️ Your turn
- In your own words, what's the difference between HTML, CSS, and JS?
- Paste your first `index.html`:

## Go deeper
- MDN — How the web works → <https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web>
