# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev presentation project - a modern slide deck framework for developers that uses Markdown to create presentations. The project contains a presentation about AI assisted software development history and timeline.

## Commands

Development and build commands:
- `pnpm install` - Install dependencies
- `pnpm dev` - Start development server (opens automatically at http://localhost:3030) (user handles this - DO NOT run this command)
- `pnpm build` - Build presentation for production
- `pnpm export` - Export slides to PDF/images

**Important:** The development server is managed by the user. If you cannot access slides with Playwright, inform the user that they should start the dev server rather than attempting to start it yourself.

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

**MANDATORY Verification Process:**
1. Make changes to slides.md
2. **IMMEDIATELY verify with Playwright** - navigate to the slide
3. Test each click/interaction step by step
4. Take screenshots at each state  
5. Verify the final visual result matches expectations
6. Fix any errors found and re-verify

**Why this is mandatory:**
- Catches syntax errors (missing `</style>` tags, Vue parsing issues)
- Prevents content overflow and layout problems
- Ensures slides work in actual presentation environment
- Maintains professional presentation quality

**Never skip this step** - slides that haven't been Playwright-verified should be considered incomplete.

## Common Issues and Solutions

**Content Overflow Issues:**
When creating content-heavy slides (like the "Prompting: Clear and Precise" slide), content may overflow beyond the visible slide area, causing important information to be cut off.

**Symptoms:**
- Content appears truncated at the bottom of slides
- Only partial sections visible during presentation
- Missing interactive elements or text

**Solution Strategy (PREFERRED APPROACH):**
1. **Split into multiple slides**: Create continuation slides with the same title plus "(2/2)", "(3/3)", etc.
2. **Optimize content hierarchy**: Prioritize essential information and shorten headings
3. **Maintain proper spacing**: Keep readable font sizes and adequate spacing for presentation clarity
4. **Test with Playwright**: Always verify content visibility with screenshot testing after changes

**Example Fix Applied:**
- Split "Prompting: Clear and Precise" into two slides
- First slide: "Acronyms and technical terms" + "Ask for positives instead of negatives"
- Second slide: "Prompting: Clear and Precise (2/2)" with "Bolster your command with a reason" + "Avoid absolutes"
- Restored proper spacing and font sizes for presentation readability
- Each slide contains 2 principles with full examples

**What to avoid:**
- ❌ Prefer avoiding scrollbars (`overflow-y: auto`) in presentations as they're not suitable for live presentation flow
- ❌ Compressing content to unreadable sizes reduces presentation effectiveness
- ❌ Very small fonts can be hard to read from audience viewing distances

**Prevention:**
- Plan content density during slide creation
- Use progressive disclosure (v-click) to reveal content gradually
- Always test slide content visibility with Playwright verification workflow
- Consider audience viewing distance when sizing text and elements