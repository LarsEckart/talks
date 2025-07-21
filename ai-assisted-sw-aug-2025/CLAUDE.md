# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

Read SLIDEV_STYLING_GUIDE.md for copy-paste patterns that maintain consistency while working within Slidev's architecture.

## Project Overview

This is a Slidev presentation project - a modern slide deck framework for developers that uses Markdown to create presentations. The project contains a presentation about AI assisted software development history and timeline.

## Commands

- `pnpm build` - Build presentation for production

**Important:** The development server is managed by the user. If you cannot access slides with Playwright, inform the user that they should start the dev server rather than attempting to start it yourself.

Presentation navigation:
- Access presenter mode: Press `P` or navigate to http://localhost:3030/presenter
- Navigation: `Space`/`Arrow Right` (next), `Arrow Left` (previous), `O` (overview), `F` (fullscreen)

## Architecture

**Slidev Framework Structure:**
```
your-slidev/
  ├── components/       # custom components
  ├── layouts/          # custom layouts
  ├── public/           # static assets
  ├── setup/            # custom setup / hooks
  ├── snippets/         # code snippets
  ├── styles/           # custom style
  ├── index.html        # injections to index.html
  ├── slides.md         # the main slides entry
  └── vite.config.ts    # extending vite config
```

Key directories:
- `slides.md` - Main presentation configuration with frontmatter and slide imports
- `slides/` - Individual slide files (e.g., `01-title.md`, `02-content.md`) imported via `src:` directive
- `pages/` - Additional slide pages (imported via `src:` directive)
- `components/` - Vue components usable in slides (e.g., Counter.vue)
- `snippets/` - External code snippets referenced in slides
- `public/` - Static assets including images referenced with `/filename.jpg` paths
- Theme: Uses 'seriph' theme with customizable layouts and styling

**Built-in Layouts Summary:**
Basic layouts: `default`, `center`, `none`. Structure layouts: `cover`, `intro`, `section`, `end`. Content emphasis: `fact`, `quote`, `statement`. Media layouts: `image`, `image-left/right`, `iframe`, `iframe-left/right`. Columns: `two-cols`, `two-cols-header`. Each layout serves specific presentation purposes.

*

## Development Workflow

**Verification with Playwright (MANDATORY):**
**EVERY slide creation or modification MUST be verified with Playwright before considering the work complete.** This is not optional - it catches syntax errors, layout issues, and ensures presentation quality.

Always use Playwright to:
- Navigate to the affected slides
- Test click interactions and v-click animations
- Verify visual transitions and scaling effects
- Take screenshots to confirm layout and positioning
- Ensure all interactive elements work as expected
- **Catch Vue parsing errors and missing tags that break slides**

The development server runs at `http://localhost:3030` and Playwright can access slides directly via URL patterns like `/4` for slide 4, with click states via `?clicks=N` parameters.
