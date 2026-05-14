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

## Troubleshooting

If the workflow fails at `Setup Pages` with `Get Pages site failed` or `HttpError: Not Found`, GitHub Pages is not enabled for the repository yet.

Fix it in GitHub:

1. Open the repository on GitHub.
2. Go to `Settings > Pages`.
3. Under `Build and deployment`, set `Source` to `GitHub Actions`.
4. Re-run the failed workflow.

The `actions/configure-pages` action has an `enablement` option, but it requires a Personal Access Token or GitHub App token with Pages/admin permissions. The default `GITHUB_TOKEN` is not enough to enable Pages for a repository.
