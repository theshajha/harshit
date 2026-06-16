# 04 — Responsive Design

> One line: making one page look good on every screen — phone, tablet, laptop.

## The idea
Most people will see your site on a phone. **Responsive design** means the layout adapts to the screen size instead of breaking. The tools: relative units (%, `rem`) instead of fixed pixels, flexible layouts (flexbox/grid that wrap), and **media queries** that apply different CSS at different widths. Rule of thumb: design for the small screen first, then add rules for bigger ones.

## Quick reference

```css
/* the one tag that makes phones behave — put in <head> */
<meta name="viewport" content="width=device-width, initial-scale=1.0">

/* media query: apply CSS only above a width */
@media (min-width: 768px) {
  .container { display: flex; }   /* side-by-side on tablet+ */
}

/* prefer flexible units */
width: 100%;          /* not 600px */
max-width: 600px;     /* cap it on big screens */
font-size: 1rem;      /* scales better than px */

/* let grids adapt automatically */
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
```

## Worked example
*(complete after you try it)*
```css
.card { width: 100%; max-width: 400px; margin: 0 auto; }
```

## Gotchas
- **Forget the `<meta viewport>` tag and phones zoom out** and render tiny — it's the #1 "why does my site look weird on mobile?" cause.
- Test by resizing your browser narrow, or use the device toolbar in browser DevTools (F12).

## ✍️ Your turn
- What does a media query do, in your words?
- Paste a responsive tweak you made:

## Go deeper
- MDN — Responsive design → <https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design>
