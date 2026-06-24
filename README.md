# Knuppel Trainer

A single-file, offline-first training logger for heavy-club / frustum work:
per-set timer + set duration, rest countdown with auto-chain, rep steppers
(no typing), work capacity, and optional per-set camera clips saved to your
phone.

- **App:** [`index.html`](index.html) — one self-contained file, vanilla JS, no
  dependencies, no backend.
- Data (sets + settings) lives in `localStorage`; recorded clips live in
  IndexedDB on the device.

## Use it on your phone

1. Open the published https URL in **Safari** (see *Hosting* below).
2. **Share → "Add to Home Screen"** → it opens full-screen like an app.
3. Tap **🎥 film sets** → allow camera access (first time only).

## Hosting (the camera needs https)

`getUserMedia` (the in-app camera) only works in a **secure context** — i.e. an
**https** URL or `localhost`. Opening the file as `file://` shows a banner and
disables the camera, but **all logging still works**.

This repo is published with **GitHub Pages**: Settings → Pages → *Deploy from a
branch* → `main` / `/ (root)`. The live URL is then:

```
https://<your-username>.github.io/<repo>/
```

## Update the app later

Edit `index.html`, then:

```bash
git add index.html
git commit -m "tweak"
git push
```

GitHub Pages redeploys automatically within ~1 minute.
