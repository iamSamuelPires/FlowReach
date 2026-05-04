# Contributing to Flowreach

Thanks for taking the time to look at the code. Contributions are welcome — this is a solo project built in public and any help improving it is appreciated.

---

## What's useful

**Bug reports** — If something doesn't work, open an issue. Include your browser, OS, and what you were doing when it broke.

**Feature requests** — Open an issue describing what you'd want and why. Practical things that fit the core use case (Outscraper → call/text → track) are most likely to get built.

**Pull requests** — Fork the repo, make your change in `flowreach.html`, and open a PR with a clear description of what changed and why.

---

## How the code is structured

Everything lives in `flowreach.html`. It's one file — no build step, no bundler, no framework.

The file is split into three sections:

1. **CSS** (inside `<style>`) — design tokens at the top as CSS variables, then component styles
2. **HTML** (inside `<body>`) — sidebar, views (upload, prospects, statistics, guide, etc.), modals
3. **JavaScript** (inside `<script>` at the bottom) — all logic, localStorage, rendering

Key functions to know:
- `processFile()` — handles file import and column mapping
- `renderTable()` — renders the prospects table from active batch data
- `renderStats()` — renders the statistics view
- `renderBatchList()` — renders the sidebar batch list
- `copySms()` — copies a personalised SMS to clipboard
- `COLUMN_DEFS` — defines which columns are imported and displayed
- `pipelineStages` — the CRM pipeline configuration

---

## Ground rules

- Keep it a single file. No build process, no npm, no external JS dependencies added to the repo.
- Keep it Outscraper-specific. This tool is intentionally narrow — it's not a general-purpose CRM.
- No server-side code. Everything must run in the browser with no backend.
- Test in Chrome and Safari before submitting.

---

## Questions

Reach out before building something large — easier to align first.

- X: [@iamsamuelpires](https://x.com/iamsamuelpires)
- LinkedIn: [Samuel Pires](https://www.linkedin.com/in/samuel-pires-4b3073267/)
