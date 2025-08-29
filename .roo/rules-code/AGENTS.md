# Project Coding Rules (Non-Obvious Only)

- Static images must live in `static/img` and are imported with require('@site/static/...').default (see [`src/components/HomepageFeatures/index.js:8`]) — do not import from relative paths outside `static`.
- Use theme components where used: e.g., use `Heading` from `@theme/Heading` in React components (see [`src/components/HomepageFeatures/index.js:2`]) to preserve site styles.
- Component CSS uses CSS Modules with the `.module.css` pattern (see [`src/components/HomepageFeatures/styles.module.css:1`]) — global CSS goes in [`src/css/custom.css:1`].
- Docs rely on numeric frontmatter `sidebar_position` for ordering (see [`docs/planning/getting-a-visa.md:2`]); changing these numbers reorders the sidebar.
- Docs category pages are created via `_category_.json` (see [`docs/arriving/_category_.json:1`]) — edit this file to change label/position or to enable generated-index metadata.
- There are no test/lint scripts in [`package.json:5`] — adding tests requires adding scripts and dependencies; CI assumes Node >=18 (see [`package.json:41`]).