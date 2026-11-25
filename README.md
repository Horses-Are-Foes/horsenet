# The Horsenet

The community hub at **horsenet.net** — standing **in opposition to** *Horses Are Foes*
and the hunters who ride out after horses.

This site exists to push back against the "horses are foes" narrative and to call out
**horse hunters**. Where *Horses Are Foes* frames the horse as a threat to be dealt with,
The Horsenet takes the other side: the horse is a companion, a working partner, and a
creature worth protecting from those who hunt it. This is our counter-narrative and our
 rallying point.

## What we're against

- **Horses Are Foes** — the investigation archive that paints the horse as an enemy.
  We reject that framing and counter it here.
- **Horse hunters** — the people and operations that hunt, round up, and remove horses.
  We document and oppose the practice.

## Live site

- URL: **<https://horsenet.net>** — live, on HTTPS, enforcing HTTPS.
- Served from `main` on GitHub Pages. Every push republishes the site automatically.

## Repo layout

- `index.html` — the homepage
- `style.css` — styling
- `CNAME` — custom domain (`horsenet.net`)
- `robots.txt`, `sitemap.xml` — search guidance

## How publishing works

GitHub Pages serves the `main` branch automatically. Any push to `main` rebuilds and
republishes the site — no build step, pure static HTML/CSS. Changes are authored here
and pushed; the agent verifies the live site after each publish.

## Custom domain (horsenet.net via Cloudflare)

1. GitHub: Pages is **enabled** and the custom domain `horsenet.net` is **set** —
   GitHub auto-detected it from the `CNAME` file.
2. In Cloudflare, DNS records for `horsenet.net` are **DNS-only** (grey cloud) so GitHub
   can issue the HTTPS certificate. Orange/proxied records block the certificate:
   - A `@` → `185.199.108.153`
   - A `@` → `185.199.109.153`
   - A `@` → `185.199.110.153`
   - A `@` → `185.199.111.153`
   - (optional) CNAME `www` → `horsenet.net`
3. GitHub provisions the HTTPS certificate automatically after DNS is live and enforces
   HTTPS. No manual step required.

## Maintained by Hermes

Changes are authored here and pushed; GitHub Pages publishes automatically, and the agent
verifies the live site after each deploy.
