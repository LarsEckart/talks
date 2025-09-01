---
layout: default
---

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 2rem;
}
</style>

# The Solution: Subagents

## Separate Context Windows for Complex Tasks

<v-click>

<div class="mt-8 p-6 bg-red-50 rounded-xl border-2 border-red-300">
<h3 class="text-2xl font-bold text-red-700 mb-4">⚠️ The Problem</h3>
<p class="text-lg text-gray-700">These "garbage tokens" muddy the agent's ability to parse what matters and maintain the entire corpus of work</p>
</div>

</v-click>

<v-click>

<div class="mt-8 p-6 bg-blue-50 rounded-xl border-2 border-blue-300">
<h3 class="text-2xl font-bold text-blue-700 mb-4">✅ The Solution</h3>
<p class="text-lg text-gray-700 mb-4"><strong>Parallelizing and managing context isn't just for users—agents need it too.</strong></p>
<ul class="text-left text-gray-600 space-y-2 ml-4">
  <li>Spawn subagents with fresh context windows for specific tasks</li>
  <li>Returns only relevant findings to the main conversation</li>
</ul>
</div>

</v-click>

<!--
Speaker notes:

This is the key architectural insight that makes tools like Claude Code or Amp so effective.

The main agent delegates exploratory work to subagents. For example:
- A subagent might read 50 files searching for a specific pattern
- Another might run dozens of test commands to debug an issue
- Each returns only the essential findings, not the entire search process

This approach mirrors how we manage memory in programming - treating context as a finite resource that needs careful allocation.

It's the only scalable way to handle complex, multi-file tasks without losing track of the overall goal.
-->
