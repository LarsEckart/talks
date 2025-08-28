# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Core Architecture

This is a Slidev presentation framework project focused on AI-assisted software development. The architecture follows a modular slide approach:

- **Main entry point**: `slides.md` contains Slidev frontmatter configuration and slide references
- **Individual slides**: `slides/` directory contains standalone markdown files, each representing one slide
- **Slide inclusion**: Each slide is referenced in `slides.md` using `src: ./slides/filename.md` format
- **Theme configuration**: Uses `apple-basic` theme with slide-left transitions

## Essential Development Commands

```bash
# Start development server (auto-opens at localhost:3030)
npm run dev

# Build static site for production
npm run build

# Export presentation to PDF/images (requires Playwright)
npm run export

# Install dependencies
npm install
```

## Slide Structure & Content Organization

**Slide format**: Each slide file starts with Slidev frontmatter (`---\nlayout: default\n---`) followed by markdown content. Speaker notes are included as HTML comments (`<!-- -->`).

### Image-Right Layout Scaling Issue & Solution

**Problem**: Slidev's `image-right` or `image-left` layout automatically scales images to fill the available space, often causing cropping of important content at edges.

**Solution**: Add white padding to images using macOS `sips` command:
```bash
# Add 100px padding on all sides to prevent cropping
sips --padToHeightWidth [original_height+200] [original_width+200] --padColor FFFFFF input.png --out output-padded.png
```

**Example**:
```bash
# For a 707x517 image, add 200px total padding (100px each side)
sips --padToHeightWidth 717 907 --padColor FFFFFF public/agentsmd.png --out public/agentsmd-wide-padded.png
```

This ensures all content remains visible when Slidev scales the image to fit the layout constraints.

## Adding New Slides

1. Create new `.md` file in `slides/` directory using kebab-case naming
2. Include Slidev frontmatter header with layout specification
3. Add slide reference to `slides.md` in desired presentation order
4. Use consistent formatting: `# Title`, bullet points, speaker notes as comments
