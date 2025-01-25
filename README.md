# Ospack Formulae

[Ospack Formulae](https://ospack.github.io) is an online package browser for [Ospack](https://ospack.sh).

It displays all packages in the [Ospack/ospack-core](https://github.com/Ospack/ospack-core) and [Ospack/ospack-cask](https://github.com/Ospack/ospack-cask). A [GitHub Action](https://github.com/Ospack/ospack.github.io/blob/master/.github/workflows/tests.yml) is run periodically which pulls changes from each tap and deploys the site to GitHub Pages.

## JSON API
It also provides a JSON API for all packages (or individual packages) in each tap and their related analytics. This JSON data is used for the creation of the HTML resources on this site.

Currently available:

- List metadata for all formulae and casks
- Get metadata for each formula and cask
- List analytics events for all formulae and casks
- List analytics events for each formula and cask

Read more in the [JSON API documentation](https://ospack.github.io/docs/api/).

## Usage
Open <https://ospack.github.io/> in your web browser.

To instead run the site locally, run:
```bash
git clone https://github.com/Ospack/ospack.github.io
cd ospack.github.io
rake generate
bundle install
bundle exec jekyll serve
```

## Search
Search is indexed by Algolia crawler at https://crawler.algolia.com/admin/crawlers/26b9e6e2-bce4-4f42-9930-6b6ddf06cc9e/overview.
This is only accessible by ospack organisation members.

## License
Code is under the [BSD 2-clause "Simplified" License](LICENSE.txt).
