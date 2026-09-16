# henrikblomfelt.com

Static single-page site. No build step, no dependencies.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole site — markup, styling and the Zürich clock |
| `portrait.jpg` | The About photo. **Must be added — see below** |
| `favicon.svg` | Browser tab icon — **placeholder** |
| `apple-touch-icon.png` | Icon when saved to an iPhone home screen — **placeholder** |
| `robots.txt`, `sitemap.xml` | Search engines |

## Add the portrait

`index.html` expects a file named `portrait.jpg` next to it. Save your
photo with that exact name and upload it to the repo. Roughly 900×1200
(3:4) is plenty; anything larger just costs load time.

Any image format works if you change the filename in `index.html` to
match (search for `portrait.jpg` — it appears twice, once in the
`<img>` tag and once in the `og:image` meta tag).

## Swap the favicon

Both icon files are placeholders (a plain "HB" mark). To replace them:

1. Export your icon as a square PNG at 512×512 and name it
   `apple-touch-icon.png`.
2. Export the same thing at 32×32 named `favicon.png`.
3. Upload both, delete `favicon.svg`, and change the icon line in
   `index.html` to:

   `<link rel="icon" href="favicon.png" type="image/png">`

An SVG works too if you have one — keep the filename `favicon.svg` and
nothing in `index.html` needs changing.

## Add a release

Find the `#work` section and copy one of the `<a class="row">` blocks.
Four things to change: the `href`, the tag word, the title, the credit.

The tag colour comes from the second class on the `<span class="tag …">`
— `release`, `studio`, `label`, `mix` or `radio`.

## Deploy

Cloudflare Pages, connected to this repo. Build command: none. Output
directory: `/`. Every push to `main` redeploys in about 30 seconds.
