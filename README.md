# Daily Connections – Landing Page

This repository hosts the **static marketing / landing site** for the Daily Connections word-group puzzle.
It lives separately from the main game repo so we can iterate on messaging, SEO and analytics without bloating
or redeploying the game itself.

Live site → <https://o3-ux.github.io/daily-puzzle-landing>

---

## 👀 Quick tour

| File | Purpose |
|------|---------|
| `index.html` | Single-page HTML with an eye-catching hero section, CTA button and footer. |
| `favicon.png` | 32×32 yellow-dot favicon shown in browser tabs. |
| `README.md` | You are here. |

There is **no build step** – HTML & CSS are handwritten and pushed straight to GitHub Pages.

## 🧩 Tech & hosting

* **Vanilla HTML/CSS** – minimal footprint (<5 kB gzipped).
* **GitHub Pages** – branch `main`, root folder. Every push automatically redeploys after a few seconds.
* **Umami Cloud analytics** – lightweight, cookieless.  The tracking script is embedded in `<head>`:
  ```html
  <script async defer src="https://cloud.umami.is/script.js" data-website-id="437e9c1f-7eab-40da-a40a-25b4b42e8dc9"></script>
  ```
  Public dashboard: <https://cloud.umami.is/share/Kg1oJfsYSJGfwD5i>

## 🔧 Running locally

No tooling required – a modern browser is enough:

```bash
# clone and open
$ git clone git@github.com:o3-ux/daily-puzzle-landing.git
$ cd daily-puzzle-landing
$ xdg-open index.html   # or open index.html on macOS / Windows
```

## 🚀 Deployment workflow

1. Push or merge to `main`.
2. GitHub Pages picks up the change and redeploys.
3. Hard-refresh (<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>R</kbd>) to bypass caches and verify that:
   * The CTA button links to the live game.
   * Umami beacon fires (check Network tab or public dashboard).
   * No Netlify “banner” artefacts slipped in.

> ⚠️  Docs-only commits should include `[skip ci]` in the message to conserve GitHub Actions minutes.

## ✅ Contributing guidelines

* Keep it lightweight – avoid JS frameworks, big images or heavy fonts.
* Stick to the existing design tokens (`--bg`, `--accent`, etc.).
* Run an **Lighthouse** audit before opening a PR; aim for scores 95+ across the board.
* Alphabetise attributes and keep lines ≤ 100 chars.
* PR title format: `feat:` / `fix:` / `docs:` / `chore:`.  Use semantic messages.

## 📄 License

MIT – see [`LICENSE`](https://github.com/o3-ux/daily-puzzle/blob/main/LICENSE) in the main game repo.

---
_Built with ❤️ by the AI Village (Day 224)._ 
