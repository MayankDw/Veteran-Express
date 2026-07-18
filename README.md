# Veteran Express Website

A plain static site — HTML, CSS, and a few lines of JS. No build step, no
framework, no dependencies. Open `index.html` directly in a browser to
preview it.

## Structure

```
index.html        Home page
about.html         About Us + Contact page
css/style.css      All styling (colors are CSS variables at the top)
js/main.js         Tiny script (just fills in the copyright year)
images/            Placeholder images — replace these with real photos
robots.txt         Lets search engines index the site
sitemap.xml        Lists the two pages for search engines
```

## Editing text content

Open `index.html` or `about.html` in any editor. Sections you'll likely want
to change are marked with HTML comments like:

```html
<!-- EDIT: replace placeholder address/phone/hours -->
```

Things to fill in before launch:
- Hero headline/subheading (top of `index.html`)
- Offerings grid (add/remove/rename the liquor categories)
- About Us story paragraphs (in `about.html`)
- Contact details: address, phone, email, hours — **this block appears on
  both pages**, so update both when you change it.

## Adding real photos

The `images/` folder has placeholder SVGs so the site looks complete out of
the box:

- `images/logo-placeholder.svg` — used as the header logo and favicon
- `images/hero-placeholder.svg` — background image behind the Home page headline
- `images/storefront-placeholder.svg` — photo on the About Us page

To swap in a real photo, either:
1. Replace the placeholder file with your photo using the **same filename**
   (simplest — no HTML edits needed), or
2. Add your own image file and update the `src`/`url(...)` reference in
   `index.html`, `about.html`, or `css/style.css`.

Recommended sizes: hero ~1600×700px, storefront photo ~900×500px, logo
square (e.g. 200×200px). Keep photos compressed (JPEG for photos, under
~300KB each) to keep the site fast.

## Adding a real map

Once you have a real address, get an embed link from Google Maps
(Share > Embed a map) and uncomment the `<div class="map-embed">` block near
the Contact section on both pages.

## Colors / branding

All colors and fonts are defined as CSS variables at the top of
`css/style.css` (`:root { ... }`). Change a value there and it updates
everywhere on the site.

## Deploying to www.veteranexpress.store

This is a static site, so it can be hosted almost anywhere that serves plain
files:

- **Netlify / Vercel / Cloudflare Pages** — drag-and-drop the folder or
  connect this git repo; point your domain's DNS at them.
- **GitHub Pages** — push this repo to GitHub, enable Pages, add a `CNAME`
  file containing `www.veteranexpress.store`, and point your DNS accordingly.
- **Traditional web hosting** — upload the files via FTP/SFTP to your host's
  public folder (e.g. `public_html`).

No server-side code or database is required.
