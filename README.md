# Chippy Helpers

Phone-first builder helpers: **spirit level**, **slope / fall**, and **balustrade bay layout**.

Static HTML/JS — no build step. Intended for Android Chrome via GitHub Pages, Add to Home Screen.

## Live

Once Pages is enabled on the repo:

**https://azzabazza11.github.io/chippy-helpers/**

## Local

```bash
cd chippy-helpers
python3 -m http.server 8080
```

Open **http://localhost:8080/** — spirit level sensors need a **secure context** (`https://` or `http://localhost`). On a phone over LAN Wi‑Fi, use GitHub Pages HTTPS (or an HTTPS local server) so orientation works.

## Tools

### Level — Spirit

- Uses `deviceorientation` (permission prompt on some browsers)
- Bubble + roll/pitch degrees
- **Calibrate** zeros against the current phone attitude
- Screen wake lock while running

### Level — Slope

- Rise/fall and run (mm) → % grade, 1:x, angle, fall per metre
- Inverse: known run + target 1:x → required rise/fall

### Balustrade

- Overall run (centre-to-centre of end posts), post centres **or** bay count
- Post width → clear opening between faces
- Baluster width + max clear gap (default **100 mm**)
- Equal gaps: balusters per bay, totals, pass/fail vs max gap
- Simple one-bay elevation sketch

## Android

1. Open the Pages URL in **Chrome**
2. Menu → **Add to Home screen** / Install app
3. For a stuck old cache, use **Reload** on the hub (unregisters the service worker and clears caches)

## Files

| File | Role |
|------|------|
| `index.html` | Hub + both tools |
| `manifest.webmanifest` | PWA install |
| `service-worker.js` | Offline cache; network-first for HTML |
| `icon.svg` | App icon |

Version: **1.0.1**
