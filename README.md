# Rackit Day Trading

One-page site for the family live trading stream.

See it, Rackit, stack it, it's done.

Entertainment only, not financial advice.

## Preview

From this folder:

```bash
python3 -m http.server 8080
```

Then open http://127.0.0.1:8080/

## GitHub Pages

`.github/workflows/pages.yml` deploys the site on every push to `main`. The build job uploads the site, and a second job deploys that artifact. GitHub Pages cannot see an artifact uploaded in the same job.

Published URL: https://ddunsford.github.io/rackit-day-trading/

Image, font, and stylesheet paths are relative, so they resolve on that project URL.

After this workflow is on `main`, set **Settings → Pages → Build and deployment → Source** to **GitHub Actions** if it is not already. The workflow passes `enablement: true` to `actions/configure-pages`. The default `GITHUB_TOKEN` is not allowed to turn Pages on by itself, so that settings step is still required the first time. If the first run stops on “Create Pages site failed”, set the source, then re-run the workflow.
