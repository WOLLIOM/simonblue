# Simon Maxam — Field Notes

A single-file personal index / hub site. Distinct "drafting sheet / cyanotype" identity,
kept separate from the SIMAX studio site.

- `index.html` — the whole site (no build step, no dependencies except Google Fonts).

## Deploy to GitHub Pages

All the URLs in this project assume the repo is named **`simonmaxam`** under the
account **`wolliom`**, so the live URL is `https://wolliom.github.io/simonmaxam/`.
If you use a different repo name, find-and-replace that URL across `index.html`,
`robots.txt`, and `sitemap.xml`.

1. Create a repo named `simonmaxam`, push this folder to it.
2. Repo → **Settings → Pages** → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Wait ~1 min, then open `https://wolliom.github.io/simonmaxam/`.

### Then submit to Google

1. Go to [Google Search Console](https://search.google.com/search-console) → add a
   **URL prefix** property for `https://wolliom.github.io/simonmaxam/`.
2. Verify with the **HTML tag** method — it gives you a `<meta name="google-site-verification" ...>`
   tag; paste it into the `<head>` of `index.html`, push, then click Verify.
3. **Sitemaps** → submit `sitemap.xml`.
4. **URL Inspection** → enter your URL → **Request indexing**.

## Edit

Everything is in `index.html`:
- Copy lives in the `<main>` section.
- Projects are `<li>` rows in `<ol class="work">` — title, blurb, spec, and the `href`.
- Colors/fonts are CSS variables at the top of `<style>`.

## To fill in later

- If the repo name isn't `simonmaxam`, update the live URL everywhere (see Deploy above).
- Add the Google Search Console verification meta tag (see below).
- Confirm the Bonterra live URL (currently links the GitHub repo).
- Swap in project images if you want thumbnails on hover.

## SEO / identity

The `<head>` includes a JSON-LD `Person` block with `sameAs` links to your SIMAX site,
Instagram (`/simonmaxam/`), LinkedIn (`/in/simonmaxam/`), and GitHub (`wolliom`). That's the
mechanism that connects your profiles into one search identity. Contact email: `simon@scalex.ink`.
