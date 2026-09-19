# Mukoma Stock & Credit

A fast, mobile-first **progressive web app (PWA)** for **Mukoma General Dealers** —
tracking retail **inventory** and **customer credit** from your phone.

Installable on Android, iOS, and desktop. Works offline.

## Features

- Retail inventory tracking
- Customer credit / debt tracking
- Offline-ready (service worker + app shell)
- Installable PWA (manifest + icons, standalone mode)
- Mobile-first, portrait-optimized UI

## Tech stack

- **Vite + React** (built static bundle in `assets/`)
- **PWA:** `manifest.webmanifest`, `sw.js` service worker
- Pure client-side — no backend required

## Run it

Built static site — just serve the folder, or open `index.html`:

```bash
# any static file server works, e.g.
npx serve .
```

For development, the source build re-runs through Vite:

```bash
npm install
npm run dev      # development (not in this repo; rebuild)
npm run build    # outputs the production bundle in assets/
```

## Install on a phone

1. Open the hosted URL in Chrome / Safari.
2. **Add to Home Screen** (Android: menu → "Add to Home screen"; iOS: Share → "Add to Home Screen").
3. Launchs fullscreen from the home screen like a native app.

## Repository layout

```
index.html               app shell
assets/                  built JS + CSS bundle
manifest.webmanifest     PWA manifest (Mukoma Stock & Credit)
sw.js                    service worker (offline support)
icons/                   app icons (192 / 512 / maskable)
favicon.svg, icons.svg
```