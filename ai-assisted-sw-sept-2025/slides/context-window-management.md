---
layout: default
---

# Context Window Management

<v-clicks depth="2">

<div class="grid grid-cols-2 gap-6 mt-8">
  <div class="p-6 bg-gray-50 rounded-lg border-2 border-gray-300">
    <h3 class="text-xl font-bold text-gray-700 mb-2">📁 Long File Contents</h3>
    <p class="text-gray-600">Reading multiple files fills context with potentially irrelevant code</p>
  </div>
  <div class="p-6 bg-gray-50 rounded-lg border-2 border-gray-300">
    <h3 class="text-xl font-bold text-gray-700 mb-2">💬 Verbose Output</h3>
    <p class="text-gray-600">Bash commands returning pages of logs and debug information</p>
  </div>
  <div class="p-6 bg-gray-50 rounded-lg border-2 border-gray-300">
    <h3 class="text-xl font-bold text-gray-700 mb-2">❌ Failed Attempts</h3>
    <p class="text-gray-600">Error messages and unsuccessful tool calls that remain in history</p>
  </div>
  <div class="p-6 bg-gray-50 rounded-lg border-2 border-gray-300">
    <h3 class="text-xl font-bold text-gray-700 mb-2">🔄 Repetitive Back-and-Forth</h3>
    <p class="text-gray-600">Multiple rounds of clarification that could be avoided</p>
  </div>
</div>

</v-clicks>

<!-- 
Speaker notes:

Context window pollution happens when agents accumulate "garbage tokens" that clutter the conversation context.

Context window pollution is a critical challenge in agent development that many developers overlook. 

When agents perform exploratory tasks like searching through codebases or running verbose commands, they accumulate "garbage tokens" - information that was necessary for a specific subtask but clutters the main conversation context.

Think of it like having too many browser tabs open - eventually, you can't find what you need because there's too much noise.

The solution is architectural: spawn subagents with their own context windows for specific tasks. The subagent can read 50 files and run 20 commands, then return only the relevant findings to the main agent.

This is exactly how tools like Cursor's Composer and Claude's Task tool work - they parallelize work across separate contexts to maintain clarity in the main conversation.

Key insight: Just as we manage memory in programming, we need to manage context in AI systems. It's a finite resource that needs careful allocation.
-->