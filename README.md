# Re:Form — landing page (deployable build)

`index.html` is fully self-contained: fonts, runtime and styles are inlined. Photographs
load from Unsplash's CDN, so the page needs a network connection to show its imagery.

## Deploy

**GitHub Pages**
1. Commit `index.html` to the repo root (or a `/docs` folder).
2. Settings → Pages → Source: `main` branch, root (or `/docs`).
3. Site goes live at `https://<user>.github.io/<repo>/`.

**Anywhere else** — Netlify, Vercel, Cloudflare Pages, S3: drop the file in.

## The CTA links

Every "Build my plan" button points at `app/` (a relative path), which works if you deploy
the planner into an `/app` subfolder of the same site. If the planner lives on its own
domain or repo, send the live URL over and the build will be regenerated pointing at it.

## Notes

- Photographs are Unsplash, free for commercial use, no attribution required (credited in
  the footer anyway).
- Icons are Phosphor, loaded from unpkg.
- Copy states plainly that nothing is sold and no supplements are pushed — keep that true.
# Re-Form-Website
