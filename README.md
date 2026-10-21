# projectAlamo website

Static landing page for projectAlamo, served by GitHub Pages at https://www.projectalamo.com.au.

## Files
- `index.html` – the whole page (styles inline, no build step)
- `CNAME` – tells GitHub Pages to serve the site on `www.projectalamo.com.au` (the bare domain redirects to it)
- `favicon.png`, `assets/` – logo, social preview image, app icon

## Publish on GitHub Pages
1. Create a new **public** repository on GitHub, e.g. `projectalamo-site`.
2. Upload every file in this folder to the root of the repo (Add file → Upload files), keeping the `assets` folder.
3. Repo **Settings → Pages**: Source = *Deploy from a branch*, Branch = `main`, folder `/ (root)`. Save.
4. Under **Custom domain**, confirm `www.projectalamo.com.au` is shown (it's read from `CNAME`).

## Point the domain (at your .com.au registrar's DNS settings)
| Type  | Host / Name | Value |
|-------|-------------|-------|
| A     | @           | 185.199.108.153 |
| A     | @           | 185.199.109.153 |
| A     | @           | 185.199.110.153 |
| A     | @           | 185.199.111.153 |
| CNAME | www         | `ealingcastre.github.io` |

Remove any existing A records or "parked page" forwarding on `@` first.

DNS can take up to 24–48 hours. Once GitHub shows the domain as verified, tick **Enforce HTTPS** in Settings → Pages.

Optional but recommended: verify the domain under your GitHub account (Settings → Pages → Add a verified domain) so nobody else can claim it.

## Editing
- Contact email: search `hello@projectalamo.com.au` in `index.html`.
- Product cards: the `<a class="card">` blocks in the Products section. When Farenwide launches, change `Coming soon` to `Available now` and remove the `soon` class.

## Brand
Colours (CSS variables at the top of `index.html`), sampled from the logo:
navy `#1D4779` (fortress), deep navy `#112A4E` (headings), blue `#205189`
("project"), sky `#5B86C4` (circuit lines), red `#BC251C` ("Alamo"), and the
arc's red-to-coral gradient (`#BC251C` → `#EE8A6A`) used for accents.
Background `#F7F8FA`. Headings in Outfit, body in Inter.

`assets/logo.png` is the logo on a transparent background, for light
backgrounds only (the white "A" is see-through). Icons (`favicon.png`,
`assets/apple-touch-icon.png`, `assets/icon-512.png`) are the emblem without
the wordmark.
