# Project agent memory

This file is the project's committed home for project-intrinsic agent knowledge: build, test, release, architecture, and sharp-edge notes that should travel with the code.

- Add durable project-specific notes here as they are discovered through real work.

## Site structure

- GitHub Pages **user site**: served from the repo root of `main`. `index.html` takes precedence over `README.md`. No build step, no framework — a single self-contained `index.html` with a few lines of inline CSS.
- **Design is deliberately plain (captain's explicit choice):** Craigslist-style — white background, black text, classic blue underlined links, plain text lists under small headings, no cards/hero/icons/dark-mode. Do not "improve" it toward a designed look.
- Projects are one `<li>` per project (link — one-line description) under the `<!-- PROJECTS -->` comment; add/delete a line to change the list.
- **No email on the page** — captain removed it on purpose; contact is the GitHub profile link only.
- Card blurbs were taken from the live GitHub repo descriptions (`gh api repos/gapsong/<name> --jq .description`). `lichess-kill-anim` has **no** GitHub description; its card links to its showcase page at `https://gapsong.github.io/lichess-kill-anim/` (built separately in its own repo's Pages).
- Do not feature the upstream forks (peft, transformers, optimum, IsaacLab, and also **axi** — it's a fork of kunchenguid/axi, …) as own projects. Merged upstream PRs belong in the "open source contributions" section instead (currently the two huggingface/peft PRs #2571 and #2664).

## Redesign variants (2026-08)

- `variants/` holds three standalone redesign candidates (a-minimal, b-editorial, c-playful) plus an index page; same content as the live `index.html`, look only differs. Self-contained (inline CSS, no CDNs), responsive, dark/light via `prefers-color-scheme`.
- The live root `index.html` stays untouched until the captain picks a direction; the chosen variant then replaces it in a follow-up (and `variants/` can be removed).
- Keeping content in sync: any project added to the live list must be added to each variant too (they duplicate the data on purpose — no build step).
