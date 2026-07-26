# Isaac Jung — Personal Portfolio

A minimal, editorial personal website for Isaac Jung, a Statistics & Machine Learning student at Carnegie Mellon University.

Built as a set of static HTML pages styled with Tailwind CSS (compiled to a static stylesheet) in a "Paper & Grid" design system — see [DESIGN.md](DESIGN.md).

## Pages

| Page | File |
|------|------|
| Home | [`index.html`](index.html) |
| About | [`about.html`](about.html) |
| Projects / Selected Works | [`projects.html`](projects.html) |
| Experience | [`experience.html`](experience.html) |

`resume.pdf` is the downloadable résumé linked from the About and Experience pages.

## Styling / build

Tailwind is **compiled to a static `styles.css`** (committed to the repo) rather than loaded from the runtime CDN, so visitors download ~20 KB of CSS instead of a ~400 KB in-browser compiler. Design tokens live in [`tailwind.config.js`](tailwind.config.js).

If you edit the HTML and add new Tailwind classes, rebuild the stylesheet:

```bash
npm install        # first time only
npm run build      # regenerates styles.css (minified)
# npm run watch    # rebuild on every save while developing
```

Commit the regenerated `styles.css` alongside your HTML changes.

## Running locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Hosted with GitHub Pages, served from the `main` branch root. Because `styles.css` is committed, no build runs on GitHub's side — remember to `npm run build` before pushing HTML/class changes.
