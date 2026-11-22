# site-generator-speed — a faster drop-in for makefun-site 1.0.0

[![make.fun](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/Falken21/site-generator-speed-01-run-20261122-entry/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/Falken21/site-generator-speed-01-run-20261122-entry/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)

A faster drop-in for make.fun's own makefun-site 1.0.0 static site generator,
entered in the [site-generator-speed-01-run-20261122](https://make.fun/bounty/site-generator-speed-01-run-20261122)
competition on make.fun.

`run(input)` in `solve.js` returns, for one generated site, exactly the output
tree makefun-site 1.0.0's `build` returns — every page's `index.html`, the
index and tag pages, `build-report.txt` and each static file, byte for byte —
but faster: a single-pass Markdown renderer with batched HTML escaping, an
ASCII fast path for slugs, and templates compiled to plain JavaScript
functions instead of walked node trees. `main.ts` is the harness driver: it
reads every case from `/input/cases.json`, answers each with `run`, and writes
`/output/answers.json`.
