# Saurabh Vishwakarma — Portfolio

Personal portfolio site for **Saurabh Vishwakarma**, engineer and team lead. Built as a
static site with plain HTML, CSS, and JavaScript — no framework, no build step.

## Run it locally

```bash
npm install         # first time only, pulls http-server as a dev dep
npm start           # serves at http://localhost:8080 and opens a tab
```

Any change to a file under this directory is picked up on refresh
(the dev server runs with caching disabled).

## Project structure

```
.
├── index.html            # main landing page (all in one file, inline JS)
├── styles.css            # main stylesheet (was neo-styles.css)
├── images/               # everything the site references
│   ├── favicon.png
│   ├── 1.png             # hero avatar
│   ├── 2.png             # journey / map illustration
│   └── …                 # legacy assets kept for reference
├── terminal/             # separate interactive terminal résumé page
│   ├── index.html        # served at /terminal/
│   ├── script.js
│   └── styles.css
├── sitemap.xml
├── robots.txt
├── package.json
├── LICENSE               # MIT
└── README.md
```

The main site is `index.html`. The interactive terminal at `terminal/` is a
separate experience that used to be linked from the footer; it's currently
unlinked (kept in the repo, out of the main navigation).

## External dependencies

Loaded from CDNs at runtime — no bundler:

- Google Fonts — Space Grotesk, Space Mono, Caveat

The map's tile layer is Stadia Maps (Stamen Watercolor); on tile errors the
site falls back to CARTO's Voyager tiles automatically.

## Deploying

Because the site is static, any static host works — GitHub Pages, Netlify,
Vercel, Cloudflare Pages, etc. Point the host at this directory as the site
root; no build command is required. The `.nojekyll` file at the root tells
GitHub Pages to skip the Jekyll pipeline.

## License

MIT — see [LICENSE](LICENSE).
