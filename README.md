# CatalystOS — Company Platform Launcher

A single self-contained HTML page. No build step, no dependencies — all fonts, images, and styles are inlined into `index.html`.

## Deploy to GitHub Pages
1. Create a new repository and upload these files (keep the structure).
2. In the repo: **Settings → Pages**.
3. Under **Build and deployment**, set **Source: Deploy from a branch**.
4. Choose branch **main** and folder **/ (root)**, then **Save**.
5. Your page will be live at `https://<username>.github.io/<repo>/` in a minute or two.

## Files
- `index.html` — the entire page (self-contained; open it directly in any browser).
- `.nojekyll` — tells GitHub Pages to serve files as-is.

## Local preview
Just double-click `index.html`, or run any static server:
```
npx serve .
```
