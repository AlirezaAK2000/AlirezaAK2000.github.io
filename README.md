# Alireza Akhoundi — academic website

Personal academic website built from [al-folio](https://github.com/alshedivat/al-folio), retaining its theme, responsive layouts, dark mode, and search.

**Intended address:** https://alirezaak2000.github.io/ (available after you publish).

## Publish to GitHub Pages

Follow [the step-by-step publishing guide](docs/GITHUB_PAGES.md). Publish the contents of this `website/` checkout as their own repository named `AlirezaAK2000.github.io`.

## Edit your website

| Content                          | File                  |
| -------------------------------- | --------------------- |
| Biography and research interests | `_pages/about.md`     |
| Research and manuscript status   | `_pages/research.md`  |
| Project descriptions             | `_projects/*.md`      |
| Teaching                         | `_pages/teaching.md`  |
| Tutorials                        | `_pages/tutorials.md` |
| CV                               | `_data/cv.yml`        |
| Email and social links           | `_data/socials.yml`   |
| Site title, address, and options | `_config.yml`         |

The homepage portrait is `assets/img/prof_pic_1.jpeg`, configured in `_pages/about.md`. To replace it, update that image or change `profile.image` to another file in `assets/img/`. Set `profile.image_circular: true` for a circular crop.

The CV is an HTML page. To offer a PDF, add a public-facing PDF at `assets/pdf/Alireza-Akhoundi-CV.pdf` and set `cv_pdf: /assets/pdf/Alireza-Akhoundi-CV.pdf` in `_pages/cv.md`.

## Local preview

On this Mac, the dependencies have been installed locally. Run `./bin/preview` from this directory, then open http://127.0.0.1:4000/ .

Use Ruby 3.3+ and Node.js 22. With Ruby and Bundler available:

```sh
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve --baseurl ""
```

Open http://127.0.0.1:4000/ . Stop with Ctrl+C. Restart the server after editing `_config.yml`.

For a production build:

```sh
JEKYLL_ENV=production bundle exec jekyll build --baseurl ""
```

Build output is in `_site/`; dependency and build folders are ignored by Git.

## Content decisions

- Background facts were reconciled against the latest background records on 18 October 2026.
- M.Sc. completion is expected in January 2027.
- The thesis manuscript is **in preparation**; it is not presented as a publication.
- Only documented public project URLs are linked. No private thesis repository is referenced.
- Phone numbers, reference contact details, test scores, and application-specific wording were omitted from this public-facing version.
- Demo biography, publications, projects, news, media, and unrelated upstream automation were removed.
- No theme runtime overrides were introduced. The blank `baseurl` is intentional for a `username.github.io` user site.

See `LICENSE` for the upstream MIT license and `docs/` for retained al-folio documentation.
