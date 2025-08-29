# Project Debug Rules (Non-Obvious Only)

- Broken links cause build failures (onBrokenLinks="throw" in [`docusaurus.config.js:33`]) — check link integrity before CI.
- Web assets must exist under `static/` or require() calls in components will fail at build time (see [`src/components/HomepageFeatures/index.js:8`]).
- Docusaurus dev server must be run from project root (scripts in [`package.json:5`] expect CWD to be repository root).
- No extra debug flags or custom logging framework configured — rely on standard Docusaurus dev server logging.