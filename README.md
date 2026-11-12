# APSInsight — public information website

Agriculture Service of Product Farm (ASPF)

Static public site for **APSInsight**, the agricultural data analytics engine at [SbruiceS/APSInsight](https://github.com/SbruiceS/APSInsight).

This repository does **not** contain the engine, farm records, tokens, threat-model exploit notes, or model weights.

## Security posture

- No JavaScript, no cookies, no forms, no third-party resources
- Content-Security-Policy via meta: `default-src 'none'`, same-origin styles and images only, no `unsafe-inline`
- `security.txt` at `.well-known/security.txt`
- Private vulnerability reports only (see `SECURITY.md`)
- `main` is protected against force-push and deletion
- GitHub secret scanning and push protection are requested on the repository
- CI (`site-guard`) rejects scripts, remote URLs and inline handlers

GitHub Pages serves the site from the root of `main` over HTTPS. GitHub, not this repo, sets transport headers such as HSTS.

## Status source

Public counts match `docs/STATUS.md` on engine commit `1c6f324` (2026-10-15): 1,590 tested, 908 partial, 224 specified, 378 blocked, of 3,100 features.

## Licence

Website text and markup: Apache-2.0, same family as the engine. The engine itself remains in its own repository.

Published from branch main.
