# Quarto Slides Template

This folder contains a minimal Quarto + Reveal.js slide deck and a GitHub Actions workflow to publish to GitHub Pages.

## Use this template

1. Copy the contents of this `template/` folder into the root of your new repository (or move the whole folder and rename it as your repo root).
2. Push to `main` on GitHub.
3. The included workflow publishes to the `gh-pages` branch automatically. In your GitHub repo settings, set Pages source to `Deploy from a branch` → `gh-pages`.

## Files

- `_quarto.yml` — Quarto project config (applies the NCSU theme and reveal options)
- `slides/index.qmd` — Starter slide deck
- `slides/theme/ncsu.scss` — Theme stylesheet
- `.github/workflows/deploy-page.yml` — GitHub Pages deployment workflow
- `.gitignore` — Ignore Quarto build artifacts and generated HTML

## Local preview

Install Quarto: https://quarto.org/docs/get-started/

Then from the project root:

```bash
quarto preview
# or
quarto render && open slides/index.html
```

## Customize

- Edit `slides/index.qmd` front matter (title, author, logo, etc.)
- Add or remove slides with `---` separators
- Tweak theme in `slides/theme/ncsu.scss`


