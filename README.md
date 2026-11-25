# horenethub

Home page for **horsenet.net**, hosted on **GitHub Pages**.

## Live site

- URL: <https://horsenet.net> (once DNS is wired — see below)

## Repo layout

- `index.html` — the homepage
- `style.css` — styling
- `CNAME` — custom domain (`horsenet.net`), required for Pages

## How publishing works

GitHub Pages serves the `main` branch automatically. Any push to `main`
rebuilds and republishes the site — no build step required (pure static HTML/CSS).

## Custom domain (horsenet.net via Cloudflare)

1. In GitHub: repo **Settings → Pages → Custom domain** → set `horsenet.net` → Save.
2. In Cloudflare: add DNS records for `horsenet.net`, set them to **DNS-only**
   (grey cloud) so GitHub can issue the HTTPS certificate:
   - A `@` → `185.199.108.153`
   - A `@` → `185.199.109.153`
   - A `@` → `185.199.110.153`
   - A `@` → `185.199.111.153`
   - CNAME `www` → `Lowebrew.github.io`
3. Wait a few minutes, then enable **Enforce HTTPS** in the Pages settings.

## Maintained by Hermes

Changes are made here and pushed; GitHub Pages publishes automatically.
