# 02 — CSS: Styling & the Box Model

> One line: CSS controls how things *look* — and the single most important idea is that every element is a **box**.

## The idea
CSS rules **select** elements and **style** them. You target an element (by tag, class, or id) and set properties (colour, font, spacing). The mental model that unlocks layout: **every element is a rectangular box** made of four layers — content, then **padding** (space inside), then **border**, then **margin** (space outside). Almost all "why is there a gap / no gap?" confusion is the box model.

## Quick reference

```css
/* selector { property: value; } */
p            { color: #333; font-size: 16px; }   /* by tag */
.intro       { font-weight: bold; }              /* by class  -> class="intro" */
#hero        { background: navy; }                /* by id     -> id="hero" */

/* the box model */
.card {
  padding: 16px;          /* space INSIDE the box */
  border: 1px solid #ccc;
  margin: 24px;           /* space OUTSIDE the box */
  box-sizing: border-box; /* makes width include padding+border — set this globally */
}

/* common properties */
color, background, font-size, font-family, font-weight
width, height, max-width
text-align, line-height
border-radius, box-shadow
display: block | inline | flex | none
```

Link CSS from your HTML `<head>`:
```html
<link rel="stylesheet" href="style.css">
```

## Worked example
```css
body { font-family: system-ui, sans-serif; line-height: 1.6; color: #222; }
.card {
  max-width: 400px;
  padding: 24px;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}
```

## Gotchas
- **Set `box-sizing: border-box`** (on `*`) early — otherwise padding makes boxes wider than the `width` you set, and layouts feel "off."
- A **class** (`.name`, reusable) vs an **id** (`#name`, one per page) — prefer classes.
- Margins can "collapse" (two stacked margins merge into the bigger one) — a classic surprise.

## ✍️ Your turn
- Explain the box model (content/padding/border/margin) in your words:
- Paste a styled element you made:

## Go deeper
- Josh Comeau — The CSS box model → <https://www.joshwcomeau.com/css/>
