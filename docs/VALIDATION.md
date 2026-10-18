# Website validation

Checked on 18 October 2026.

- Production Jekyll build: passed, with an empty base URL for the GitHub Pages user site.
- Local runtime: Ruby 4.0.6 and Node.js 22.19.0; dependencies installed inside this checkout. GitHub Actions is configured to use Ruby 3.3 and Node.js 22.
- Prettier: passed.
- al-folio starter style contract: passed.
- al-folio upgrade audit: zero blocking and zero non-blocking findings.
- Generated content: 14 HTML pages, with no missing local link or asset targets.
- Demo/private-content scan: no sample biography, Einstein publications, example PDF, template portrait, or private thesis repository URL in generated pages.
- Local preview: returned HTTP 200. The preview server was stopped after verification; restart it with `./bin/preview`.
- Browser visual review: incomplete. Browser automation reported a native-pipe failure, so layout, mobile interaction, and dark-mode interaction have not been visually verified.
- GitHub publication: not performed. The supplied workflow will run after the prepared checkout is pushed to your website repository and GitHub Pages is enabled.

No local theme runtime overrides were introduced.
