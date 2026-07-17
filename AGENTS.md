# Project agent memory

This file is the project's committed home for project-intrinsic agent knowledge: build, test, release, architecture, and sharp-edge notes that should travel with the code.

- Add durable project-specific notes here as they are discovered through real work.

## Site structure

- GitHub Pages **user site**: served from the repo root of `main`. `index.html` takes precedence over `README.md`. No build step, no framework — a single self-contained `index.html` with inline CSS (system fonts, light/dark via `prefers-color-scheme`).
- Project cards live in `index.html` inside the `<!-- PROJECT CARDS -->` comment block: one `<article class="card">` per project, page order = source order. To add/remove a project, copy/delete a block.
- Card blurbs were taken from the live GitHub repo descriptions (`gh api repos/gapsong/<name> --jq .description`). `lichess-kill-anim` has **no** GitHub description; its card links to its showcase page at `https://gapsong.github.io/lichess-kill-anim/` (built separately in its own repo's Pages).
- Do not feature the upstream forks (peft, transformers, optimum, IsaacLab, …) as own projects.
