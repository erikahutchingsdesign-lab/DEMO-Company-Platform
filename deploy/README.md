# Havener Studio — Marketing & Sales Launcher

An iPad-style app launcher for the Havener Capital marketing & sales team. Big app
icons open a client picker; selecting a client launches that client's app/demo.

Everything is contained in a single file: **`index.html`** (logo, fonts, and all
icons are embedded — no build step, no asset folder).

## Deploy

Pick any one of these. All of them serve `index.html` as the home page automatically.

### Netlify (drag & drop — easiest)
1. Go to https://app.netlify.com/drop
2. Drag the whole `deploy/` folder onto the page.
3. Done — you get a live URL. Optional: set a custom domain in Site settings.

### Vercel
```bash
npm i -g vercel
cd deploy
vercel        # follow prompts; accept defaults
vercel --prod # publish to production
```

### GitHub Pages
1. Create a new repo and push these files (see below).
2. Repo → Settings → Pages → Source: `main` branch, `/ (root)`.
3. Your site goes live at `https://<user>.github.io/<repo>/`.

### Cloudflare Pages / AWS S3 / any static host
Upload `index.html`. That's it.

## Push to GitHub

```bash
git init
git add .
git commit -m "Havener Studio launcher"
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```

## Updating app links

The launcher links out to client apps/demos (Webinar Graphics, Social Graphics, the
Client Dashboard, etc.). Those URLs live inside the app's logic. To change them,
edit the source `Havener Studio.dc.html` in the design tool, re-export the standalone
file, and replace `index.html` here.

## Notes
- The greeting ("Good morning, Havener team") adapts to the time of day.
- Active apps/clients are marked green.
- External app links open in a new tab and must remain hosted/reachable to work.
