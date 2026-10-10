# fuzzley.github.io

Publishes [fuzzley.info](https://fuzzley.info) with GitHub Pages.

The site's source lives in [fuzzley/fuzzley](https://github.com/fuzzley/fuzzley).
This repository only holds the deploy workflow,
[`.github/workflows/pages.yml`](.github/workflows/pages.yml), which builds that
source and publishes it. fuzzley/fuzzley triggers it after every push to its
`main` branch and waits for it, so a failed deploy shows on that commit too;
it can also be run by hand from the Actions tab.

Settings it depends on:

- **Settings → Pages → Source:** GitHub Actions.
- **Settings → Pages → Custom domain:** fuzzley.info, with HTTPS enforced.
- **Repository variable `GA_AG_MEASUREMENT_ID`:** the Google Analytics 4
  measurement ID. Leave it unset to publish with analytics off.
