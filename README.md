# Personal Site

Static site (plain HTML/CSS/JS, no build step) for personal branding and SEO.

**Status: live** at [bbysolution.com](https://bbysolution.com), deployed on Netlify from this repo's `main` branch.

## Content

- `index.html` holds all copy: About, Expertise, AI Advisory, Career timeline, 8 featured projects, Tools, Education, Awards, Contact, and a full 78-row work-experience attachment table.
- `<title>` / `<meta name="description">` and the `application/ld+json` Person block (top of `<head>`) drive the Google search snippet / knowledge-panel data — update these first if the pitch changes.
- `assets/img/favicon.png` and `assets/img/og-cover.jpg` are already in place.
- To add more profiles (X/Twitter, GitHub, etc.), extend the `sameAs` array in the JSON-LD block.

## Local preview

No build tools needed. Either:
- Open `index.html` directly in a browser, or
- Run a local server so relative paths behave exactly like production:
  ```
  npx serve .
  ```

## Deployment

Connected: pushing to `main` on `bby-debug/bbysolution-com` auto-deploys to Netlify, which serves `bbysolution.com` directly (build command empty, publish directory `.` per `netlify.toml`).

The contact form uses **Netlify Forms** (`data-netlify="true"`) — submissions show up under **Site settings → Forms** in the Netlify dashboard. No backend needed.
