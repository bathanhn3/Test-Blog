# Test-Blog

Basic static blog using Jekyll and GitHub Pages.

## Local development

Install Ruby, then run:

```bash
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000/Test-Blog/`.

## Deploy to GitHub Pages

This repo includes `.github/workflows/pages.yml`.

1. Push to `main` or `master`.
2. In GitHub, open `Settings > Pages`.
3. Set `Build and deployment > Source` to `GitHub Actions`.
4. The workflow builds the Jekyll site and deploys it to GitHub Pages.

If this repository is renamed or deployed as a user site like `username.github.io`, update `baseurl` in `_config.yml`.
