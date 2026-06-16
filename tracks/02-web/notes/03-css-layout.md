# 03 — CSS Layout: Flexbox & Grid

> One line: how you arrange boxes on the page — flexbox for rows/columns, grid for two-dimensional layouts.

## The idea
Once elements are styled boxes (note 02), **layout** is about positioning them. Modern CSS gives you two tools: **flexbox** (lay items out in a row or column, with smart spacing — great for navbars, button groups, centering) and **grid** (rows *and* columns at once — great for page layouts and card galleries). Flexbox is the one you'll use most; learn it first.

## Quick reference

```css
/* FLEXBOX — one direction (row or column) */
.row {
  display: flex;
  gap: 16px;                    /* space between items */
  justify-content: center;      /* align along the main axis (space-between, etc.) */
  align-items: center;          /* align along the cross axis */
  flex-direction: row;          /* or column */
  flex-wrap: wrap;              /* let items wrap to next line */
}

/* GRID — two dimensions */
.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);   /* 3 equal columns */
  gap: 16px;
}

/* the classic "center anything" */
.center { display: flex; justify-content: center; align-items: center; }
```

## Worked example
*(complete after you try it)*
```css
nav { display: flex; gap: 24px; align-items: center; }
```

## Gotchas
- `justify-content` vs `align-items`: one is the main axis, the other the cross axis. With `flex-direction: row`, justify = horizontal, align = vertical. Swap when it's `column`.
- Use `gap`, not margins, for spacing between flex/grid items — much cleaner.

## ✍️ Your turn
- When do you reach for flexbox vs grid, in your words?
- Paste a layout you built:

## Go deeper
- Flexbox: <https://flexbox.io> / CSS-Tricks "A Complete Guide to Flexbox"
