# Simon Maxam — Field Notes

A single-file personal index / hub site. Distinct "drafting sheet / cyanotype" identity,
kept separate from the SIMAX studio site.

- `index.html` — the whole site (no build step, no dependencies except Google Fonts).

## Deploy (Cloudflare Pages)

- **Source repo:** `WOLLIOM/simonblue`
- **Live URL:** `https://simonmaxam.pages.dev/` (this new hub site replaced the old SIMAX
  portfolio at that URL). All URLs in `index.html`, `robots.txt`, `sitemap.xml` point here.
- **Old SIMAX portfolio** now lives at `https://simax.rf.gd/` — the hub links to it.

Plain HTML site, **no build step**. Cloudflare Pages build config:

| Field | Value |
|---|---|
| Framework preset | None |
| Build command | **empty** (delete `npm run build`) |
| Build output directory | **`/`** (not `out`) |
| Root directory | blank |

Push to `main` → deploys automatically.

### Then submit to Google

`simonmaxam.pages.dev` already has a Search Console property with 1 indexed page — reuse it.

1. **Sitemaps** → submit `sitemap.xml`.
2. **URL Inspection** → `https://simonmaxam.pages.dev/` → **Request indexing**
   (do this again after the new content deploys so Google re-crawls it).

## Edit

Everything is in `index.html`:
- Copy lives in the `<main>` section.
- Projects are `<li>` rows in `<ol class="work">` — title, blurb, spec, and the `href`.
- Colors/fonts are CSS variables at the top of `<style>`.

## To fill in later

- If you add a custom domain later, find-and-replace `https://simonmaxam.pages.dev/` everywhere.
- Confirm the Bonterra live URL (currently links the GitHub repo).
- `simax.rf.gd` (free InfinityFree host) often blocks search crawlers with a 403 — if you
  want the old SIMAX portfolio indexed too, move it to Cloudflare Pages / Netlify.
- Swap in project images if you want thumbnails on hover.

## SEO / identity

The `<head>` includes a JSON-LD `Person` block with `sameAs` links to your SIMAX site,
Instagram (`/simonmaxam/`), LinkedIn (`/in/simonmaxam/`), and GitHub (`wolliom`). That's the
mechanism that connects your profiles into one search identity. Contact email: `simon@scalex.ink`.
