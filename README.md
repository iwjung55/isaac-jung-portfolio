# Isaac Jung — Personal Portfolio

A minimal, editorial personal website for Isaac Jung, a Statistics & Machine Learning student at Carnegie Mellon University.

Built as a set of static HTML pages styled with Tailwind CSS (via CDN) in a "Paper & Grid" design system — see [DESIGN.md](DESIGN.md).

## Pages

| Page | File |
|------|------|
| Home | [`index.html`](index.html) |
| About | [`about.html`](about.html) |
| Projects / Selected Works | [`projects.html`](projects.html) |
| Experience | [`experience.html`](experience.html) |

`resume.pdf` is the downloadable résumé linked from the About and Experience pages.

## Running locally

It's plain static HTML — open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Hosted with GitHub Pages, served from the `main` branch root.
