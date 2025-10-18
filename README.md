# Milan Gogolin — Portfolio

This is a small static portfolio site (plain HTML/CSS/JS) intended to be hosted on GitHub Pages.

Repository layout

- `index.html`           — main site page (no build step)
- `viewer.html`          — optional viewer page (unused)
- `css/style.css`        — site styles
- `assets/`              — images, videos, logos, and `project-assets.json`
	- `project-assets.json` — machine-readable list of project asset filenames
	- `Resume.pdf`         — PDF resume opened from the About page

Quick notes for GitHub Pages

- The site uses relative paths (e.g., `assets/...` and `css/style.css`) so it will work when served from the repository root on GitHub Pages.
- Files and filenames are case-sensitive on GitHub Pages (Linux). The manifest `assets/project-assets.json` matches the exact filenames currently in `assets/`.
- To publish on GitHub Pages from this repository (recommended):
	1. Commit and push your changes to the `main` branch.
	2. In your repository Settings -> Pages, choose `main` as the source and `/ (root)` as the folder.
	3. Save. GitHub will give you a URL (it may take a minute to provision).

Optional improvements

- Convert `assets/project-assets.json` entries to typed objects like `{ "src": "assets/P1-4.mp4", "type": "video" }` and update the page JS to rely on the `type` field. This removes extension-based heuristics.
- Normalize filenames to consistent casing (e.g., `jpg` vs `JPG`) to avoid confusion when editing from case-insensitive OSes.

If you'd like, I can make the typed-manifest change and update `index.html` to use `type` fields (small patch).
