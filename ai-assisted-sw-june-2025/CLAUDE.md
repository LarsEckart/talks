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
- `slides.md` - Main presentation configuration with frontmatter and slide imports
- `slides/` - Individual slide files (e.g., `01-title.md`, `02-content.md`) imported via `src:` directive
- `pages/` - Additional slide pages (imported via `src:` directive)
- `components/` - Vue components usable in slides (e.g., Counter.vue)
- `snippets/` - External code snippets referenced in slides
- `pictures/` - Image assets referenced with `/pictures/filename.jpg` paths
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
- Individual slides in `slides/` directory have their own frontmatter for layout and styling
- External slides imported via `src: ./slides/filename.md` directive in slide frontmatter
- **CRITICAL**: Each slide must be in its own file in the `slides/` directory - do NOT create inline slides in `slides.md`

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
1. Make changes to slide files in `slides/` directory (or add new slide imports to `slides.md`)
2. **IMMEDIATELY verify with Playwright** - navigate to the slide
3. Test each click/interaction step by step
4. Take screenshots at each state  
5. Verify the final visual result matches expectations
6. Fix any errors found and re-verify
7. Commit changes

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

## Slide Rendering Issues and Debugging

**Common Rendering Problems:**
When slides appear completely blank despite proper syntax, this often indicates fundamental structural issues that require systematic debugging.

**Symptoms of Rendering Failures:**
- Slide shows completely blank at all click states
- Title (h1) not visible even though it should appear immediately
- Content appears blank even with simplified v-click structure
- Playwright screenshots show only navigation elements

**Root Cause Analysis:**
1. **Excessive nested v-click elements**: Too many v-click attributes create complex animation sequences
2. **Structural syntax errors**: Malformed HTML or CSS can break entire slide rendering
3. **CSS conflicts**: Complex layout properties can interfere with Slidev's rendering engine
4. **Container complexity**: Overly complex flexbox/grid structures may not render properly

**Debugging Strategy (PROVEN EFFECTIVE):**
1. **Use working slide templates**: Always rebuild problematic slides using confirmed working slide structures
2. **Simplify v-click usage**: Limit v-click to major sections, not individual bullets
3. **Test incrementally**: Build slides piece by piece, testing after each addition
4. **Match proven patterns**: Copy structure from existing working slides rather than creating new patterns

**Slide Structure Best Practices:**
```markdown
---

# Title Here

<div class="content-container">
  
  <div class="section-item" v-click>
    <h3>Section Title</h3>
    <ul class="bullet-list">
      <li>Bullet point 1</li>
      <li>Bullet point 2</li>
      <li>Bullet point 3</li>
    </ul>
  </div>

  <div class="section-item" v-click>
    <h3>Second Section</h3>
    <ul class="bullet-list">
      <li>More content</li>
    </ul>
  </div>

</div>

<style>
/* Standard h1 gradient styling */
/* Container with max-width and center */
/* Section styling with backdrop effects */
</style>

---
```

**V-Click Optimization:**
- **Recommended**: 1 v-click per major content section (results in 2-3 total clicks)
- **Avoid**: Multiple v-click levels (v-click on container + v-click on each bullet)
- **Target**: Maximum 3-4 clicks for full slide revelation

**When Rebuilding Slides:**
1. **Copy working slide structure** from existing slides in the presentation
2. **Replace content** while keeping structural elements identical
3. **Test immediately** after structural changes
4. **Verify click sequence** matches expected progression

## V-Click Animation Behavior

**Important Discovery:**
V-click animations in Slidev may not always work as expected with complex nested structures. Some slides may show all content immediately rather than progressively revealing it through clicks.

**Observed Behavior:**
- Simple v-click structures work reliably for progressive disclosure
- Complex nested v-click elements may all render at once
- This doesn't affect slide functionality - content is still fully accessible
- Slides remain presentation-ready even without progressive animations

**Best Practice:**
- Focus on content quality and visual layout over animation complexity
- V-click should enhance, not be essential for, slide comprehension
- Always verify slide works well even if all content shows immediately
- Prioritize clear structure and readable content

## Slide Creation Workflow

**IMPORTANT: Proper Slide Structure**
This presentation uses a modular slide architecture where each slide is a separate file in the `slides/` directory.

**Creating New Slides:**
1. **Create slide file**: Always create new slides as separate `.md` files in `slides/` directory
2. **Naming convention**: Use numeric prefixes for ordering (e.g., `00-ai-timeline.md`, `01-title.md`)
3. **Import in slides.md**: Add slide reference using `src: ./slides/filename.md` format
4. **Never inline**: Do NOT create slide content directly in `slides.md` - this breaks the modular structure

**Example Slide Import in slides.md:**
```markdown
---
src: ./slides/00-ai-timeline.md
---

---
src: ./slides/01-title.md
---
```

**Common Mistakes to Avoid:**
- ❌ Creating inline slide content in `slides.md` between `---` separators
- ❌ Missing frontmatter `---` delimiters in slide files
- ❌ Incorrect image paths (use `/pictures/filename.jpg` not `./pictures/`)
- ❌ Forgetting to verify slide rendering with Playwright

**Image Asset Usage:**
- Store images in `pictures/` directory in project root
- Reference with absolute paths: `/pictures/filename.jpg`
- Common image formats: `.jpg`, `.png` supported
- Always include meaningful `alt` attributes for accessibility