# Re:Form — deployable build

`index.html` is fully self-contained: fonts, runtime, styles and the PNG-export library are inlined.
No build step, no server code, no API keys, no dependencies.

## Deploy

**GitHub Pages**
1. Commit `index.html` to the repo root (or a `/docs` folder).
2. Settings → Pages → Source: `main` branch, root (or `/docs`).
3. Site goes live at `https://<user>.github.io/<repo>/`.

**Anywhere else** — Netlify, Vercel, S3, Cloudflare Pages, or any static host: drop the file in and point the host at it.

**Locally** — double-click the file. It works from `file://` because everything is inlined.

## Notes

- PNG export renders at up to 8× density on desktop; phones step down to stay inside the browser canvas limit.
- PDF export uses the browser print dialog — choose "Save as PDF" as the destination.
- All plan calculations run in the browser; your inputs never leave the device.
- The optional feedback card is the one exception: if you submit it, your rating, name and the
  plan's parameters are appended as a row to the linked Google Sheet (Apps Script web app).
  Skipping the card sends nothing. See `google-apps-script.md` in the source project to
  re-point or disable it (clear `SHEET_URL`).
- "Share with a friend" uses the OS share sheet where available and an in-app share panel
  (WhatsApp, Telegram, X, email, copy link) elsewhere.
- Not medical advice. Calorie estimates use the Mifflin–St Jeor equation with standard activity multipliers.
