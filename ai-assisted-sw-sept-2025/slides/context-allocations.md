---
layout: default
---

# The Context Window Allocation Problem

- **Less is more**: Adding more tools to an LLM's context window degrades output quality and increases unexpected behavior
- **Context window reality check**: Advertised sizes are misleading - actual usable context is much smaller after system prompts
- **Practical limit**: Recommended ~100k tokens before starting fresh session

<!--
This slide addresses one of the biggest misconceptions in AI development today. Most teams think: "More tools equals more capability." But the reality from production deployments tells a different story.

I've seen enterprise teams load their AI agents with dozens of tools, then wonder why the output quality drops and the AI starts behaving unpredictably. The culprit? Context window pollution. Every tool you add takes up precious context space, and that advertised 2 million token window? In practice, you're lucky to get 100k tokens of truly usable context after system prompts and tool descriptions.

This constraint isn't a limitation - it's a design principle. The best AI agents are focused, not comprehensive.
-->