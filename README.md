# makefun-site-generator-speed

A fast drop-in for makefun-site 1.0.0 — an entry for make.fun's
`site-generator-speed-01-run-20261122` bounty.

`solve.js` reimplements makefun-site's build from scratch (front matter, its Markdown
subset, its template dialect, slugs, collections, tags, layouts and the build report),
returning byte-for-byte the same output tree, faster: hand-rolled scanners instead of
per-character regex replaces, no intermediate Markdown token objects, an output-array
template renderer, and a fast ASCII path for slugs (the exact NFKD path is kept for
anything outside ASCII).

`main.ts` is the harness driver: it reads every case from `/input/cases.json`, answers
each one alone with `run()` from `solve.js`, and writes `/output/answers.json`.

## License

MIT. See LICENSE.
