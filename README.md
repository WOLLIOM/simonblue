# Simon Maxam — Field Notes

A single-file personal index / hub site. Distinct "drafting sheet / cyanotype" identity,
kept separate from the SIMAX studio site.

- `index.html` — the whole site (no build step, no dependencies except Google Fonts).

## Deploy (Cloudflare Pages)

Repo: `WOLLIOM/simonblue`. Live URL will be `https://simonblue.pages.dev/`.
All URLs in `index.html`, `robots.txt`, `sitemap.xml` are already set to that.

This is a plain HTML site — **there is no build step**. In the Cloudflare Pages
build configuration:

| Field | Value |
|---|---|
| Framework preset | None |
| Build command | **leave empty** (delete `npm run build`) |
| Build output directory | **`/`** (root — not `out`) |
| Root directory | leave blank |

Then push this folder to `main` and it deploys automatically.

### Then submit to Google

1. [Google Search Console](https://search.google.com/search-console) → add a
   **URL prefix** property for `https://simonblue.pages.dev/`.
2. Verify with the **HTML tag** method — paste the `<meta name="google-site-verification" ...>`
   tag into the `<head>` of `index.html`, push, then click Verify.
3. **Sitemaps** → submit `sitemap.xml`.
4. **URL Inspection** → enter the URL → **Request indexing**.

## Edit

Everything is in `index.html`:
- Copy lives in the `<main>` section.
- Projects are `<li>` rows in `<ol class="work">` — title, blurb, spec, and the `href`.
- Colors/fonts are CSS variables at the top of `<style>`.

## To fill in later

- Add the Google Search Console verification meta tag (see Deploy above).
- If you add a custom domain later, find-and-replace `https://simonblue.pages.dev/` everywhere.
- Confirm the Bonterra live URL (currently links the GitHub repo).
- Swap in project images if you want thumbnails on hover.

## SEO / identity

The `<head>` includes a JSON-LD `Person` block with `sameAs` links to your SIMAX site,
Instagram (`/simonmaxam/`), LinkedIn (`/in/simonmaxam/`), and GitHub (`wolliom`). That's the
mechanism that connects your profiles into one search identity. Contact email: `simon@scalex.ink`.
