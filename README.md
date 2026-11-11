# AboutGTA — Cloud Stack HTML Package

Local files only. Nothing has been published, deployed, or uploaded from this package. No accounts were created and no credentials were used.

## Files

| File | Page | Target topic |
|---|---|---|
| `index.html` | AboutGTA hub | GTA 6 overview — launch, price, Festival, PC, map |
| `gta-6-release-date.html` | Release Date | 19 Nov 2026 launch, PS5 + Xbox Series X|S, pre-load |
| `gta-6-price.html` | Price | Standard $79.99, Ultimate $99.99, confirmed 24 Jun 2026 |
| `gta-6-festival-miami.html` | Festival | Sat 21 Nov 2026, Mana Wynwood, Miami, DICE lottery tickets |
| `gta-6-pc-system-requirements.html` | PC & System Requirements | PC unconfirmed / expected 2027, Estimated specs only |
| `gta-6-map-leonida.html` | Leonida Map | Vice City + 5 more named regions, no official map size |
| `README.md` | This file | File list, interlink map, deploy instructions |

All pages: title + meta description + H1/H2s, clean responsive CSS inline, no external JavaScript, no external images.

## Facts used — verified only

- GTA 6 launches 19 Nov 2026, PS5 + Xbox Series X|S. PC not officially confirmed, widely expected 2027.
- Price: Standard $79.99, Ultimate $99.99 US, confirmed 24 Jun 2026. Pre-orders 25 Jun 2026.
- Festival: Sat 21 Nov 2026, Mana Wynwood, Miami, presented by Rockstar + PlayStation. Lineup incl. Travis Scott, Cardi B, Don Toliver, Kodak Black. Lottery entries closed 02:00 PKT 11 Nov 2026. Winners buy on DICE from 22:00 PKT 11 Nov 2026, max 2, non-transferable, 17+ only. DICE lists $60 — labelled DICE-listed, NOT Rockstar-announced.
- 30fps: Rockstar Newswire says "targeting 30 frames per second" — NOT locked/confirmed, no 60fps mode announced, not explicitly ruled out.
- System requirements: NO official PC requirements. Estimated only: RTX 2060 / RX 5700 XT, i7-8700K, 16GB RAM, 100GB storage — labelled Estimated.
- Map: Leonida, Vice City, 6 named regions: Vice City, Leonida Keys, Grassrivers, Port Gellhorn, Ambrosia, Mount Kalaga. No official map size published.
- Pre-load: started 10 Nov 2026, reported up to ~212GB — labelled Reported.

## Target articles linked to (exact URLs only)

1. https://aboutgta.com/
2. https://aboutgta.com/release-date/
3. https://aboutgta.com/news-hub/gta-6-price-guide/
4. https://aboutgta.com/gta-6-festival-miami-november-21/
5. https://aboutgta.com/system-reqs/
6. https://aboutgta.com/release-date/map/
7. https://aboutgta.com/gta-6-pc-release-date/
8. https://aboutgta.com/gta-6-release-time/
9. https://aboutgta.com/gta-6-ps5-vs-xbox-series-xs/
10. https://aboutgta.com/jason-and-lucia-gta-vi-dual-protagonists-explained/

No other aboutgta.com URLs are used. No slugs were guessed.

## Anchor policy

- ~60% branded: "AboutGTA"
- ~20% naked URL: https://aboutgta.com/
- ~10% generic: "read the full guide"
- ~10% topical partial: e.g. "GTA 6 price guide", "Festival guide on AboutGTA"
- 0% exact-match keyword-stuffed anchors.
- Max 2 links to the same target URL per page.

## Interlink map

Every page links to every other page twice: once in the top nav, once in the "More from AboutGTA" section at the bottom.

```
index.html
  <-> gta-6-release-date.html
  <-> gta-6-price.html
  <-> gta-6-festival-miami.html
  <-> gta-6-pc-system-requirements.html
  <-> gta-6-map-leonida.html
```

Outbound links to aboutgta.com per page (see verification counts in the delivery report):
- Each page links to the homepage + at least 3 target articles.
- Topic pages link most heavily to their own matching article, plus related guides.

## Images

No image files exist in this package, and no image URLs were invented. Each page has a styled text placeholder div, e.g.:

`[Image placeholder: GTA 6 Festival Miami — Mana Wynwood stage and lineup graphic to be added]`

To add real images later:
1. Put the files in `images/` inside this `cloud/` folder, e.g. `images/festival-hero.jpg`.
2. Replace the placeholder `<div class="placeholder">…</div>` with `<img src="images/festival-hero.jpg" alt="…">`.
3. Keep filenames descriptive and use the article title as the basis for alt text. Do not hotlink images from other sites without permission.

## Deploy — same files, no build step

These are plain static HTML files. The same folder works on every host below. Pick ONE host per deployment; do not deploy the identical stack to many hosts at once without a reason — duplicate stacks add little and look spammy.

### Netlify (drag-and-drop, easiest)
1. Go to Netlify Drop (app.netlify.com/drop) or Sites → Add new site → Deploy manually.
2. Drag the whole `cloud/` folder onto the drop zone.
3. Netlify gives you a `*.netlify.app` URL. Test every page and every outbound link.
4. Optional: Site settings → Domain management to add a custom domain.

### Vercel
1. `vercel.com` → Add New → Project → import, or use the CLI: `npm i -g vercel && vercel` inside the `cloud/` folder.
2. Framework preset: Other / no framework. No build command, no output directory change.
3. Deploy, then test the `*.vercel.app` URL.

### GitHub Pages
1. Create a public repo, upload the contents of `cloud/` to the repo root (or to `docs/`).
2. Repo → Settings → Pages → Source: Deploy from a branch, branch `main`, folder `/` (or `/docs`).
3. Wait for the build, then test the `*.github.io` URL.

### Cloudflare Pages
1. Cloudflare dashboard → Workers & Pages → Create → Pages → Upload assets (direct upload).
2. Name the project, drag the `cloud/` folder in, Deploy.
3. Test the `*.pages.dev` URL.

### Firebase Hosting
1. Install CLI once: `npm install -g firebase-tools`, then `firebase login`.
2. In a project folder: `firebase init hosting` (public directory = this `cloud/` folder, single-page app: No).
3. `firebase deploy --only hosting`, then test the `*.web.app` URL.

### Surge
1. Install once: `npm install -g surge`.
2. Inside `cloud/`: `surge` — accept the suggested project path, pick a domain (e.g. `aboutgta-gta6.surge.sh`).
3. Test the Surge URL. Re-deploy with `surge` again after any edit.

### Render
1. Render dashboard → New → Static Site.
2. Connect a Git repo containing these files, or use the static-site flow: build command empty, publish directory = the folder containing the HTML files.
3. Deploy, then test the `*.onrender.com` URL.

## After deploying (checklist)

- [ ] All 6 pages load (no 404s).
- [ ] Every aboutgta.com link goes to the exact URL listed above.
- [ ] No placeholder text left visible that was meant to be replaced (unless images are intentionally still pending).
- [ ] Pages are public and crawlable (no password, no noindex added).
- [ ] Check the live URLs in Google Search Console (URL Inspection → Request Indexing) if the property is verified.
- [ ] Log the live stack URL in the AboutGTA tracker under Stack Links: platform, live URL, date live, indexed Y/N.
