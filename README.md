# fuzzley.github.io

Publishes a copy of [fuzzley.info](https://fuzzley.info) at
https://fuzzley.github.io/ with GitHub Pages. fuzzley.info is the primary
site, served by Cloud Run from fuzzley/fuzzley's Docker image; this copy does
not replace it.

The site's source lives in [fuzzley/fuzzley](https://github.com/fuzzley/fuzzley).
This repository only holds the deploy workflow,
[`.github/workflows/pages.yml`](.github/workflows/pages.yml), which builds that
source and publishes it. fuzzley/fuzzley triggers it after every push to its
`main` branch and waits for it, so a failed deploy shows on that commit too;
it can also be run by hand from the Actions tab.

Settings it depends on:

- **Settings → Pages → Source:** GitHub Actions.
- **Settings → Pages → Custom domain:** none. fuzzley.info stays on Cloud Run.
- **Repository variable `GA_AG_MEASUREMENT_ID`:** the Google Analytics 4
  measurement ID. Leave it unset to publish with analytics off.
