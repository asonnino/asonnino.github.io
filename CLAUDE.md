# Personal website — sonnino.com

Jekyll site (hacked from the Minimal Mistakes / academicpages template), deployed on
GitHub Pages at https://sonnino.com. Local preview:
`bundle exec jekyll serve --config _config.yml,_config.dev.yml`.

## How content is wired

- **Publications & tech reports** are driven by `_data/papers.json`. Each entry's
  `filename` must match a PDF in `papers/` exactly. `category` routes entries to
  `_pages/publications.md` vs `_pages/reports.md`.
- **Talks** are driven by `_data/talks.json`. The `slides` field resolves to
  `/slides/alberto-sonnino/<file>`; entries in `papers` resolve to `/papers/<file>`.
  Filenames must match disk exactly — typos become silent 404 links.
- Keep both JSON files **strict JSON** (no trailing commas). Jekyll's YAML parser
  tolerates them, but other tools choke.

## Intentional quirks — do not "fix"

- **Empty links** like `[2027]()` in `_pages/academia.md` are placeholders for
  CFP/committee pages not yet published. Leave them until the URL exists.
- **`_pages/pictures.md`** (`/pictures/`) is deliberately absent from
  `_data/navigation.yml`: it exposes the `images/Alberto Sonnino - N.jpg` photos to
  crawlers for Google Images visibility without showing them on the site.
- **Unlisted PDFs** in `papers/` (e.g. the Libra ones) are hosted on purpose even
  though no page links them. Old slide versions in `slides/` are an archive; most
  are unreferenced by design.

## Build constraints

- Keynote `*.key` sources live next to the exported PDFs in `slides/` but are
  excluded from the build (`exclude` list in `_config.yml`) to keep the deployed
  site under the GitHub Pages 1 GB limit. Keep them in the repo; never publish them.
