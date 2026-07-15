# arunmathewofficial.github.io

Academic site for Arun Mathew, published at <https://arunmathewofficial.github.io> via GitHub Pages.

Built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template, itself a fork of [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/).

## Local preview

```sh
bundle install
bundle exec jekyll serve
```

## Where the content lives

| Path | Contents |
| --- | --- |
| `_config.yml` | Site identity, sidebar profile links, publication categories |
| `_data/navigation.yml` | Header tabs |
| `_pages/about.md` | Home page |
| `_pages/research.md` | Research interests, codes, HPC, mentoring |
| `_pages/cv.md` | CV — publications, talks and teaching are generated from the collections |
| `_publications/` | One file per paper; `category:` is `manuscripts`, `conferences`, or `forthcoming` |
| `_talks/` | One file per talk |
| `_teaching/` | One file per teaching role |
| `_posts/` | Blog posts, listed under the Blogs tab |

Adding a file to a collection updates both its own page and the CV.

## Tooling

`markdown_generator/` converts BibTeX, ORCID, or TSV exports into collection
markdown in bulk — useful for importing a publication list rather than writing
each entry by hand.

`talkmap.ipynb` geocodes the `location` field of `_talks/` entries into
`talkmap/org-locations.js`, which renders the map at `/talkmap.html`. The
`.github/workflows/scrape_talks.yml` workflow runs it automatically on any push
that touches `_talks/`, and commits the result.

Both are excluded from the built site in `_config.yml`.
