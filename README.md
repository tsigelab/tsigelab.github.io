# tsigelab.github.io

Website of the Tsige Lab at the University of Akron, built with Jekyll and the [al-folio](https://github.com/alshedivat/al-folio) theme (MIT licence, see `LICENSE`). Pushing to `main` builds the site into the `gh-pages` branch, which GitHub Pages serves.

The predictor page embeds the surface tension app set by `predictor_url` in `_config.yml`. `.github/workflows/keep-awake.yml` opens the app every 6 hours so it does not fall asleep. GitHub pauses scheduled workflows after 60 days without activity in the repository; re-enable it on the Actions tab.
