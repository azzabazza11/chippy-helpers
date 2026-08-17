# ABC Done! — Free Builder Helper

Phone-first site tools: **spirit level**, **slope / fall**, and **balustrade bay layout**.

Formerly Chippy Helpers. Same URL: **https://azzabazza11.github.io/chippy-helpers/**

Static HTML/JS — no build step. Android Chrome via GitHub Pages, Add to Home Screen.

## Local

```bash
cd chippy-helpers
python3 -m http.server 8080
```

Open **http://localhost:8080/** — spirit level sensors need a **secure context** (`https://` or `http://localhost`).

## Tools

### Level — Spirit

- Uses `deviceorientation`
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
2. **Install** / Add to Home screen
3. Stuck on an old cache? **Reload**

Version: **1.2.0**
