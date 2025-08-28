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

**Current slide topics** (in presentation order):
- Introduction and agenda slides
- AI agent fundamentals and architecture
- Context window management and allocations
- Library dependency strategies
- Development workflows (Ralph method, vibecoding)
- LLM selection frameworks
- Career transformation insights
- Practical applications (MCP servers, Git workflows)
- Advanced concepts (subagents, deliberate practice)

**Slide format**: Each slide file starts with Slidev frontmatter (`---\nlayout: default\n---`) followed by markdown content. Speaker notes are included as HTML comments (`<!-- -->`).

## Adding New Slides

1. Create new `.md` file in `slides/` directory using kebab-case naming
2. Include Slidev frontmatter header with layout specification
3. Add slide reference to `slides.md` in desired presentation order
4. Use consistent formatting: `# Title`, bullet points, speaker notes as comments

## Deployment Configuration

- **Netlify**: Configured in `netlify.toml` (Node 20, SPA redirects)
- **Vercel**: Configured in `vercel.json` (SPA rewrites)
- **Build output**: Static files generated to `dist/` directory

The presentation content is derived from comprehensive analysis of AI development articles, organized into a coherent learning progression from fundamentals to advanced practices.