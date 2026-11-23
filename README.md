[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/JackEasons/makefun-site-generator-speed/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/JackEasons/makefun-site-generator-speed/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

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
