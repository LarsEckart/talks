# Repository Guidelines

## Project Structure & Module Organization
- Root entry: `slides.md` (Slidev front‑matter and deck outline).
- Embedded slides: `slides/` (kebab-case files, e.g., `what-do-we-talk-about-today.md`).
- Config: `package.json`, `netlify.toml`, `vercel.json`, `.gitignore`.
- Optional (create as needed): `components/`, `pages/`, `public/` for assets.

## Build, Test, and Development Commands
- `npm install`: Install dependencies.
- `npm run dev`: Start Slidev dev server at http://localhost:3030.
- `npm run build`: Generate static site in `dist/`.
- `npm run export`: Export to PDF/images (requires Playwright setup if prompted).

## Coding Style & Naming Conventions
- Markdown: use `#` for the slide title; concise content per slide.
- Files: kebab-case for slide files in `slides/` (e.g., `context-window-management.md`).
- Titles: Title Case in headings; keep under ~60 characters.
- Assets: place static assets in `public/` and reference with `/...` paths.
- JavaScript/Vue (if used): follow ES modules, prefer clear names over abbreviations.

## Testing Guidelines
- No formal test suite. Validate by running `npm run dev` and reviewing slides.
- Check links, images, and theme rendering. Build locally with `npm run build` before PRs.

## Commit & Pull Request Guidelines
- Commits: imperative mood and scoped, e.g., `slides: add overview`, `theme: set apple-basic`.
- Keep changes focused; include rationale in the body when non-trivial.
- PRs: clear description, screenshots or GIFs of key slides, and any preview URL.
- Link related issues. Note breaking changes in the PR description.

## Security & Configuration Tips
- Node: use v18+ locally; Netlify targets Node `20` per `netlify.toml`.
- Do not commit build artifacts (`dist/`) or exports (`slides-export/`, PDFs).
- No secrets required; avoid embedding tokens in content.

