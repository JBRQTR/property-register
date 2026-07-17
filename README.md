# The Register — installable property manager

A standalone, installable web app (PWA) for managing your properties, units,
tenants, payments, maintenance, documents and expenses. No app store, no
build tools — just open it and install it like an app.

## What's in this folder
- index.html        — the whole app
- manifest.json      — tells the browser this is an installable app
- sw.js               — service worker, lets it work offline once loaded
- icon-192.png, icon-512.png, icon-512-maskable.png, apple-touch-icon.png

## Important: hosting vs. opening the file directly
Double-clicking index.html works (all features run), but **the real "Install
App" prompt on Windows and full offline support only appear when the files
are served over a URL** (even a very simple one) — browsers block service
workers and install prompts on plain local files as a security rule.

The easiest free way to get a real URL, in about 5 minutes:

### Option A — GitHub Pages (free, permanent, works from any device)
1. Create a free GitHub account if you don't have one: https://github.com/signup
2. Create a new repository (e.g. "my-property-register"), and set it to Public.
3. Upload these 6 files (index.html, manifest.json, sw.js, and the 4 icon
   PNGs) to the repository — GitHub's web interface has an "Add file →
   Upload files" button, no command line needed.
4. In the repository, go to Settings → Pages → under "Branch" choose
   "main" → Save.
5. GitHub gives you a URL like:
   https://yourusername.github.io/my-property-register/
6. Open that URL on your iPhone (Safari) or Windows PC (Edge/Chrome):
   - iPhone: tap the Share icon → "Add to Home Screen"
   - Windows (Edge or Chrome): click the install icon in the address bar,
     or the "⋮" menu → "Apps" → "Install this site as an app"

### Option B — just open the file locally for now
Double-click index.html to try it immediately in any browser on your PC.
On iPhone, AirDrop or email the file to yourself, open it in Safari, then
"Add to Home Screen" — you'll get an app icon and full-screen view, just
without offline caching until it's hosted somewhere (Option A).

## Your data
All data is stored locally in the browser (localStorage), on whichever
device you're using. If you install it on both your iPhone and your PC,
they'll each keep their own separate copy of your data — there's no sync
between devices in this version. If you'd like the two to share one set of
data, that needs a small backend (a database Claude can help you set up
separately) — let me know if you want that added.
