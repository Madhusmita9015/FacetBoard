# FacetBoard — Production vs. Target Tracker

A single-file, browser-only tool. Upload a production report (with yellow-highlighted
cut pieces) and a target order sheet, and it tells you what's been cut vs. what's
still owed, and lets you export the matched pieces as CSV.

No backend — everything runs client-side in the visitor's browser. Nothing is
uploaded anywhere.

## Structure

```
index.html                              ← the whole app (open directly in a browser to test locally)
sample-files/
  sample-production-report.xlsx         ← example production report with highlighted rows
  sample-target-order-sheet.xlsx        ← example target order sheet
```

The upload screen has direct download links to both sample files so first-time
visitors can try the tool immediately without needing their own data.

## Deploying

**GitHub Pages**
1. Push this repo to GitHub.
2. Settings → Pages → set source to your main branch (root).
3. Live at `https://<username>.github.io/<repo>/`.

**Netlify / Vercel / Cloudflare Pages**
Drag-and-drop this whole folder (or connect the repo) — no build step needed,
it's a static site.

## Local testing

Just open `index.html` in a browser, or run a tiny local server from this folder:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.
