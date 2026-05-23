# Dryland Elite — Marketing Site

Static one-page marketing site for [Dryland Elite](https://app.drylandelite.com).

- Single `index.html` with inline CSS
- No build step, no framework
- Drop screenshots into `screenshots/` (`home.png`, `drills.png`, `battles.png`, `leaderboard.png`) and they replace the placeholder phone mockups automatically

## Local preview

Open `index.html` in a browser, or serve the directory:

```
python3 -m http.server 4000
# → http://localhost:4000
```

## Deploy — Cloudflare Pages

1. Cloudflare dashboard → **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
2. Authorize Cloudflare to access GitHub, then pick `jimtaylor104/dryland-elite-site`.
3. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave blank)*
   - **Build output directory:** `/`
4. Click **Save and Deploy**. First build takes ~30 seconds.
5. Map a custom domain in **Pages → Custom domains** if you want `drylandelite.com` to point at this instead of the `*.pages.dev` subdomain.

That's it — every push to `main` redeploys automatically.

## Screenshots

The four phone-mockup slots expect:

| File | Used in |
|---|---|
| `screenshots/home.png` | Hero + Feature 1 |
| `screenshots/drills.png` | Feature 2 |
| `screenshots/battles.png` | Feature 3 |
| `screenshots/leaderboard.png` | Feature 4 |

Until you drop these in, the slots show a labeled placeholder.
