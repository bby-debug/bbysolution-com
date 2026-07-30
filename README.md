# Personal Site

Static site (plain HTML/CSS/JS, no build step) for personal branding and SEO.

## What to edit before launch

- `index.html`
  - `<title>` and `<meta name="description">` (top of `<head>`) — this is what shows up in Google search results
  - The `application/ld+json` block — structured data Google uses to build a knowledge panel. Fill in real `sameAs` links (LinkedIn, X/Twitter, GitHub, etc.)
  - About section copy
  - Services section copy (currently drafted around AI process audits — adjust if scope changes)
  - Case Studies — replace placeholders with 1-2 real engagements once available
  - `og:image` — add a real 1200x630 image at `assets/img/og-cover.jpg` for link previews
- `assets/img/favicon.png` — add a favicon

## Local preview

No build tools needed. Either:
- Open `index.html` directly in a browser, or
- Run a local server so relative paths behave exactly like production:
  ```
  npx serve .
  ```

## Deploying to Netlify

1. Push this folder to a GitHub repo.
2. In Netlify: **Add new site → Import an existing project → GitHub** → select the repo.
3. Build settings: leave **build command** empty and **publish directory** as `.` (already set in `netlify.toml`).
4. Deploy. Netlify gives you a `*.netlify.app` URL immediately.
5. Once you own a domain: **Site settings → Domain management → Add a domain**, then point the domain's DNS at Netlify (Netlify will show you the exact records — either use Netlify DNS, or add the A/CNAME records at your registrar).
6. The contact form uses **Netlify Forms** (`data-netlify="true"`) — once deployed on Netlify, submissions show up automatically under **Site settings → Forms**. No backend needed.
