# FuelBoard — Installable PWA

This folder is a real Progressive Web App (PWA). To install it on an Android
phone with an actual home-screen icon and offline support, it needs to be
hosted on HTTPS first (phones won't install a PWA straight from a local file).

## 1. Host it (free, takes 2 minutes)

Easiest option — GitHub Pages:
1. Create a new GitHub repo (e.g. "fuelboard").
2. Upload all files in this folder (index.html, manifest.json,
   service-worker.js, icons/) to the repo root.
3. Go to Settings → Pages → set source to "main" branch, root folder.
4. GitHub gives you a URL like: https://yourname.github.io/fuelboard/

Other free options that work the same way: Netlify (drag-and-drop the folder
at app.netlify.com/drop) or Vercel.

## 2. Install on your Android phone

1. Open the hosted URL in Chrome on your phone.
2. Tap the ⋮ menu → "Add to Home screen" (or "Install app" if Chrome
   shows that banner automatically).
3. Confirm — you'll get a real icon on your home screen that opens
   full-screen, no browser bars, and works offline for everything except
   the photo scanner.

## 3. Set up the photo scanner (optional)

The scanner calls the Anthropic API directly from your phone, so it needs
its own API key:
1. Get a key at console.anthropic.com → API Keys (pay-as-you-go, photo
   analysis costs a fraction of a cent per scan).
2. In the app, open "Scanner Setup" → paste the key → Save.
   It's stored only on your device.
3. Skip this if you don't want to use the scanner — everything else
   (logging, custom dishes, recipes, day tracking) works without it.

## What works offline

- Daily meal logging, custom dish creation, recipes, day navigation,
  goals — all stored on your phone (localStorage), no internet needed
  once installed.
- Only the photo scanner requires an internet connection (it calls an
  AI vision model).
