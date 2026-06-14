# Midnight Hold'em PWA

This is your original single-file Midnight Hold'em HTML game packaged as an installable Progressive Web App.

## What's included

- `index.html` — your game file with PWA metadata and service worker registration added
- `manifest.webmanifest` — app name, icons, display mode, theme color, and install settings
- `sw.js` — offline cache/service worker
- `icons/` — generated app icons

## How to test locally

Service workers do not run from a raw `file://` URL. Serve the folder locally instead:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## How to install

Upload the folder to GitHub Pages, Netlify, Vercel, or another HTTPS host. Then:

- Desktop Chrome/Edge: open the site and click the install icon in the address bar.
- Android Chrome: open the site and choose “Add to Home screen” or “Install app.”
- iPhone Safari: open the site, tap Share, then “Add to Home Screen.”

## Updating the app

When you change files later, update `CACHE_NAME` in `sw.js`, for example:

```js
const CACHE_NAME = "midnight-holdem-v2";
```

That forces browsers to refresh the offline cache.
