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

1. In GitHub: Pages is **already enabled** and the custom domain `horsenet.net`
   is **already set** — GitHub auto-detected it from the `CNAME` file.
2. In Cloudflare: add DNS records for `horsenet.net`, set them to **DNS-only**
   (grey cloud) so GitHub can issue the HTTPS certificate. Orange/cloud-proxied
   records block the certificate:
   - A `@` → `185.199.108.153`
   - A `@` → `185.199.109.153`
   - A `@` → `185.199.110.153`
   - A `@` → `185.199.111.153`
   - (optional) CNAME `www` → `horsenet.net`
3. Once the records propagate, `horsenet.net` resolves to the site. GitHub
   provisions the HTTPS certificate automatically after DNS is live, so no manual
   "Enforce HTTPS" step is needed — the agent verifies it live and confirms.

## Maintained by Hermes

Changes are made here and pushed; GitHub Pages publishes automatically.
