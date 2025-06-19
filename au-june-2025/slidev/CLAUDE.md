# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev presentation project - a modern slide deck framework for developers that uses Markdown to create presentations. The project contains a presentation about AI assisted software development history and timeline.

## Commands

Development and build commands:
- `pnpm install` - Install dependencies
- `pnpm dev` - Start development server (opens automatically at http://localhost:3030) (i usually do this for you)
- `pnpm build` - Build presentation for production
- `pnpm export` - Export slides to PDF/images

Presentation navigation:
- Access presenter mode: Press `P` or navigate to http://localhost:3030/presenter
- Navigation: `Space`/`Arrow Right` (next), `Arrow Left` (previous), `O` (overview), `F` (fullscreen)

## Architecture

**Slidev Framework Structure:**
- `slides.md` - Main presentation content in Markdown with frontmatter configuration
- `pages/` - Additional slide pages (imported via `src:` directive)
- `components/` - Vue components usable in slides (e.g., Counter.vue)
- `snippets/` - External code snippets referenced in slides
- Theme: Uses 'seriph' theme with customizable layouts and styling

**Key Features:**
- Markdown-based slides with Vue component integration
- Interactive components and animations (v-click, v-motion)
- Code highlighting with Monaco editor support
- LaTeX and diagram support (Mermaid, PlantUML)
- Draggable elements and presenter notes
- Multiple export formats

**Slide Configuration:**
- Frontmatter in slides.md controls theme, transitions, and metadata
- Individual slides can have their own frontmatter for layout and styling
- External slides imported via `src:` directive in slide frontmatter

## Custom Timeline Component

This presentation includes custom timeline styling for history slides:

**Timeline Structure:**
- Two history slides: "History" (slide 2) and "History - 2025" (slide 3)
- Both use `.timeline-container` with proper vertical timeline styling
- Timeline items use `v-click` animations for progressive disclosure

**Important CSS Scoping Notes:**
- Slidev CSS is **per-slide scoped**, NOT global
- Each slide that uses timeline styling needs its own `<style>` block
- Both history slides contain identical CSS for consistent styling
- Timeline uses blue gradient: `#4EC5D4 → #146b8c → #4EC5D4`

**Timeline Classes:**
- `.timeline-container` - Main container with centered vertical line
- `.timeline-continued` - Modifier for continuation slides (second history slide)
- `.timeline-item` - Individual timeline entries with alternating left/right layout
- `.timeline-dot` - Timeline markers (no `.highlight` class used)
- `.timeline-content` - Content boxes with backdrop blur effects

**Content Structure:**
- History slide: June 2022 to November 2024 (5 items)
- History - 2025 slide: May 2025 to June 2025 (3 items including MCP servers)
- All timeline items use consistent `h3` (date) and `p` (description) structure

## Development Workflow

**Verification with Playwright:**
Our workflow includes verification of all slide changes using Playwright browser automation. After implementing any slide modifications (especially interactive features, animations, or styling changes), always use Playwright to:

- Navigate to the affected slides
- Test click interactions and v-click animations
- Verify visual transitions and scaling effects
- Take screenshots to confirm layout and positioning
- Ensure all interactive elements work as expected

The development server runs at `http://localhost:3030` and Playwright can access slides directly via URL patterns like `/4` for slide 4, with click states via `?clicks=N` parameters.

**Example Verification Process:**
1. Make changes to slides.md
2. Navigate to the slide using Playwright
3. Test each click/interaction step by step
4. Take screenshots at each state
5. Verify the final visual result matches expectations

This ensures all slide functionality works correctly in the actual presentation environment before delivery.