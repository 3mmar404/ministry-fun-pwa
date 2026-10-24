# Ministry of Fun Animation — Offline PWA

A bilingual Arabic / English mobile-first calculator for Disco, Tombola, animation commissions, and counting cash. Uses the original company logo supplied for this project.

## Run locally

Serve the folder through HTTP (service workers do not work on `file://`):

```bash
python -m http.server 8080
```

Visit `http://localhost:8080`. To install on mobile, deploy over HTTPS and use **Add to Home Screen** / **Install App**.

## Deploy to GitHub Pages

Create a GitHub repository, upload the contents of this folder to the repository root, then open **Settings → Pages → Deploy from a branch → main / (root)**. The relative paths support project Pages URLs. A public GitHub Pages site serves the app; it does not store your data.

## Features

- Arabic and English language switch, RTL/LTR layout
- Disco: $10/$15/$20 ticket sales; per-person commissions with editable rates; chief commission and expenses; net profit and EGP conversion
- Tombola: printed count and first serial; multiple ranges per animator; overlapping-range validation; serial-number search; tickets distributed/sold/left; expected cash (pairs at $5, odd extra at $3); actual cash handed in and difference; $1 commission per sold ticket by default
- Manual chief commission, or optional adjustable percentage (not yet confirmed as a fixed rule)
- Report screen optimized for screenshots, native share text, and browser Print/Save PDF
- USD / EGP / EUR denomination counter
- Saved reports and JSON export/import, all stored on the current device
- Offline service-worker caching after first successful load

## Notes and limits

- No server, login, synchronization, or automatic cloud backup.
- All values are user-entered. The app does not know the actual amount of money collected unless you enter it.
- Tombola expected revenue is calculated from the **number sold**, not the number initially distributed.
- Tombola per-person commission adjustments can be negative or positive.
- Disco unassigned ticket sales have no auto commission; add named people to calculate their commissions.
- The default chief percentage is only an optional estimate. Confirm actual rules before enabling it.
- The current report share action sends a textual summary; use the report view screenshot or browser Print/Save PDF for a visual report.
- Clearing browser/site data can erase local records; export backups periodically.

## Technology

Vanilla HTML, CSS, JavaScript, LocalStorage, Service Worker. No build system, external dependencies, or network API calls.


V6: USD/EUR include denomination 2, original company logo is used for installed PWA PNG icons (192/512), and footer credit: Direct by amar.
