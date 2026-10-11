# InterioX Spatial Studio — Frontend

Two ways to use this folder:

1. **standalone-single-file.html** — everything (HTML+CSS+JS) in one file.
   Just double-click it, or upload it to any static host. Easiest for a
   submission that needs "one file that just works".

2. **index.html + styles.css + app.js** — the same app split into separate
   files, for a submission that specifically asks for separate HTML/CSS/JS.
   Open index.html the same way; it loads styles.css and app.js next to it.

## Requirements
Needs an internet connection in the browser tab that opens it, because it
loads three.js, Tailwind, Google Fonts and the QR code library from public
CDNs (Three.js/QRCode from cdn.jsdelivr.net, Tailwind's play CDN, Google
Fonts). No build step, no npm install — just open the HTML file.

## What's client-side only (by design, for a static demo)
- Accounts (mobile-OTP or email/password) and saved designs live in the
  browser's localStorage — there's no server here, so they don't sync across
  devices. See ../backend for a real API that replaces this.
- Checkout is a labeled demo summary — no payment is processed.
- The designer directory and review requests (with photo upload) are stored
  locally too; see ../backend/app/routers/designers.py for the real version.
