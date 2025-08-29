# Project Documentation Rules (Non-Obvious Only)

- Intro is pinned to site root via `slug: /` in [`docs/intro.md:3`] — removing slug changes homepage routing.
- Each section uses a `_category_.json` to control label and generated index metadata (see [`docs/planning/_category_.json:1`]).
- Use numeric `sidebar_position` in frontmatter to order docs within a category (see [`docs/rooting/paying-bills.md:2`]).
- Edit links point to GitHub repo path set in `docusaurus.config.js:51` — ensure editUrl stays accurate for "Edit this page" links.

