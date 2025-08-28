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
- No formal test suite. Validate by running `npm run dev` and reviewing slides using playwright mcp.
- Check links, images, and theme rendering. Build locally with `npm run build`.

## Image Handling for Slidev Layouts

### Image-Right Layout Scaling Solution
When using `layout: image-right`, Slidev automatically scales images to fill available space, which can crop important content at edges.

**Fix**: Add white padding around images before using them:
```bash
# Use macOS sips to add padding (prevents cropping when scaled)
sips --padToHeightWidth [height+200] [width+200] --padColor FFFFFF source.png --out padded.png
```

**Workflow**:
1. Check image dimensions: `sips -g pixelWidth -g pixelHeight image.png`
2. Add 100px padding on all sides: `sips --padToHeightWidth [h+200] [w+200] --padColor FFFFFF image.png --out image-padded.png`
3. Reference padded version in slide frontmatter: `image: image-padded.png`

## Adding New Slides

1. Create new `.md` file in `slides/` directory using kebab-case naming
2. Include Slidev frontmatter header with layout specification
3. Add slide reference to `slides.md` in desired presentation order
4. Use consistent formatting: `# Title`, bullet points, speaker notes as comments
