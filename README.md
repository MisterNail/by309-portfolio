# by309 / VSTROY portfolio

Bilingual static portfolio based on v13 with the requested PIC2LUT image fixes.

- Russian: https://misternail.github.io/by309-portfolio/ru/
- English: https://misternail.github.io/by309-portfolio/

## Source and editing

The complete editable source, original assets and generated pages are in `by309-portfolio-github-pages-source.zip`. The archive has a `by309-portfolio/` top-level folder. It was uploaded as an archive to preserve all folders and binary images through the GitHub web interface.

Extract it and run the following inside `by309-portfolio/` (Python 3.12 or newer):

```sh
python scripts/build.py
python scripts/check.py
node --check dist/assets/site.js
```

Edit text and project images in `content/`, templates in `scripts/build.py`, and styles or interactions in `dist/assets/`. Keep `identity.origin` in `content/site.json` set to the published URL.

To publish an update, replace the source ZIP on the `main` branch using the same filename and top-level folder. `.github/workflows/pages.yml` extracts the archive, rebuilds both languages, checks links and assets, and publishes `dist/` to GitHub Pages. Every push to `main` starts the workflow.
