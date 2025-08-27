---
layout: default
---

# The Context Window Allocation Problem

- **Less is more**: Adding more tools to an LLM's context window degrades output quality and increases unexpected behavior
- **Context window reality check**: Advertised sizes are misleading - actual usable context is much smaller after system prompts
- **Practical limit**: Recommended ~100k tokens before starting fresh session

<!--
The author challenges the common assumption that more tools = better AI performance. This is counterintuitive but critical for enterprise deployments.
-->