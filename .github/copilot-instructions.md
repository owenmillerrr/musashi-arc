# Copilot instructions for "First Software Project"

- Repo purpose: a tiny static website with an HTML file at `First Project HTML.html` and a stylesheet in `First Project CSS`.

- Big picture: single-page static content. No build system, no package manager, no server-side code found. Edit `First Project HTML.html` for structure and `First Project CSS` for styling. When adding new assets, keep filenames simple and update the `href` in the HTML's `<link rel="stylesheet">`.

- File locations to reference:
  - `First Project HTML.html` — main page source (structure and content)
  - `First Project CSS` — stylesheet file (rename to `.css` when adding content if you create a CSS file)
  - `.vscode/` — workspace config (if present)

- Conventions discovered:
  - The HTML currently links an empty `href=""` for the stylesheet. When adding CSS, use a relative path (e.g., `First Project CSS/styles.css`) and update the `<link>` tag.
  - Keep headings and lists simple; this repo is a static educational page.

- Typical edits an AI agent should perform:
  1. Fix the stylesheet link: replace the empty `href` with a relative path to the CSS file you create (example: `href="First Project CSS/styles.css"`).
  2. Improve accessibility: add a meaningful `<title>`, `lang` attribute is already present, ensure lists have clear semantics.
  3. Preserve plain-English content tone; avoid adding frameworks or build tooling unless the user asks.

- Examples to follow:
  - To add styles, create `First Project CSS/styles.css` and reference it in `First Project HTML.html`.
  - Keep filenames with spaces only when necessary—prefer `styles.css` and move into a folder without spaces if you refactor.

- What *not* to change without asking:
  - Do not introduce package.json, node_modules, or build tooling unless user requests it.
  - Do not rename `First Project HTML.html` without confirmation; the user may rely on the current filename.

- Debugging notes for agents:
  - The project runs by opening `First Project HTML.html` in a browser (no server required). Verify local changes by reloading the file in the browser.

- If you make changes, include a short note in the PR describing what files changed and why (e.g., "Added styles.css and fixed link in HTML").

If anything here is inaccurate or you'd like more detailed rules (naming conventions, CSS style guide, or test harness), tell me what to include and I'll update this file.