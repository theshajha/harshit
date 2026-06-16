# 07 — Build & Deploy Your Portfolio

> One line: your first real project — a personal site, live on the internet, that you'll grow for years.

## The idea
A portfolio is the perfect first build: it's *yours*, it's motivating, and it forces the whole loop — write HTML/CSS, see it in the browser, put it on GitHub, deploy it live. Start small and **static (v1)**; make it real before you make it fancy. "Live on the internet" is the bar — localhost doesn't count.

## The plan

**v1 — static, this week:**
1. Make a folder `projects/portfolio/` with an `index.html`.
2. Add the basics: your name, a line about you, a photo, links (GitHub, email).
3. Style it with a `style.css` — keep it clean: one nice font, generous spacing, one accent colour.
4. Make it **responsive** (note 04) so it looks right on a phone.
5. **Deploy it** (below) and share the link.

**v2+ — later, as you learn more:**
- Add a projects section (cards linking to things you've built).
- Add a tiny bit of JavaScript (a theme toggle — notes 05/06).
- Eventually, a blog or an AI feature (this becomes your "sampler").

## Deploy it free

**GitHub Pages (easiest for static sites):**
```
1. Push your repo to GitHub.
2. Repo → Settings → Pages → Deploy from branch → main → /root.
3. Your site is live at https://<username>.github.io/<repo>/
```

**Vercel (great once you add frameworks):**
```
1. vercel.com → sign in with GitHub.
2. Import the repo → Deploy. Done — you get a live URL.
```

## Gotchas
- Name your homepage exactly **`index.html`** — hosts look for that by default.
- Use **relative** paths for images/CSS (`style.css`, not `/Users/...`) or they break once deployed.
- Don't polish forever. Ship v1 ugly-but-live, then improve. A live site beats a perfect local one.

## ✍️ Your turn
- Paste your live portfolio URL:
- One thing you'd improve in v2:

## Go deeper
- GitHub Pages → <https://pages.github.com> · Vercel → <https://vercel.com>
