# uRep website

Single-page landing site for uRep. It is self-contained: `index.html` has inline CSS and no external assets.

Intended to be published at <https://urep.dev>.

## Preview

No parent directory is needed — the site runs on its own:

```bash
cd website
docker run --rm -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
# open http://localhost:8080/
```

Or simply open `index.html` in a browser.

## Structure

```
website/
├── CNAME         # custom domain for GitHub Pages
├── index.html    # the whole single-page site
└── README.md
```

Documentation links point to the source repository:
<https://github.com/nelebadnjak/urep> (`docs/cli.md`, `docs/docker.md`, `docs/spec.md`).

## Hosting

The folder is ready for static hosting. For GitHub Pages, publish this folder as
the site root and keep `CNAME` (`urep.dev`); DNS needs a `CNAME` record for
`urep.dev` pointing to `nelebadnjak.github.io` (or the four GitHub Pages `A`
records for the apex domain).
