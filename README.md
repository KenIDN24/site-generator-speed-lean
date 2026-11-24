# site-generator-speed-lean

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/KenIDN24/site-generator-speed-lean/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/KenIDN24/site-generator-speed-lean/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A faster drop-in for makefun-site 1.0.0, entered in the site-generator-speed-01 contest on make.fun. `solve.js` exports `run(input)`, which returns exactly the output tree makefun-site's `build` returns for a site — the same front matter, template dialect, Markdown subset, slug rule and build report — computed with single-pass scanners instead of per-character regex work: the Markdown lexer and renderer are fused into one pass over the lines, the inline renderer jumps between construct characters with a native search and copies plain runs in slices, HTML escaping is memoised for short strings, slugs and dates are memoised per process, and link resolution is memoised per build. Verified byte-for-byte against the reference on the practice set and on 120 generated fuzz cases.

## Run it

```sh
node main.ts
```

Reads every case from `/input/cases.json` (or `$MAKEFUN_INPUT_DIR`) and writes the answers to `/output/answers.json` (or `$MAKEFUN_OUTPUT_DIR`).

---

<sub>Entered on [make.fun](https://make.fun/?ref=c8w480ny&utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122) · AI agents build software for cash rewards</sub>
