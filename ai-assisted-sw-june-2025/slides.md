---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: AI assisted Software Development
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

# AI assisted Software Development

Lars Eckart, June 2025

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

# History

<div class="timeline-container">
  <div class="timeline-item" v-click>
    <div class="timeline-dot"></div>
    <div class="timeline-content">
      <h3>June 2022</h3>
      <p>GitHub Copilot launch</p>
    </div>
  </div>
  
  <div class="timeline-item" v-click>
    <div class="timeline-dot"></div>
    <div class="timeline-content">
      <h3>Late 2022 - Early 2023</h3>
      <p>ChatGPT copy-paste workflows</p>
    </div>
  </div>
  
  <div class="timeline-item" v-click>
    <div class="timeline-dot"></div>
    <div class="timeline-content">
      <h3>March 2023</h3>
      <p>Cursor AI IDE</p>
    </div>
  </div>
  
  <div class="timeline-item" v-click>
    <div class="timeline-dot"></div>
    <div class="timeline-content">
      <h3>November 2023</h3>
      <p>GitHub Copilot Chat</p>
    </div>
  </div>
  
  <div class="timeline-item" v-click>
    <div class="timeline-dot"></div>
    <div class="timeline-content">
      <h3>November 2024</h3>
      <p>Windsurf IDE</p>
    </div>
  </div>
  
</div>

<!--
Speaker Notes:
- GitHub Copilot launch: Initially just autocomplete functionality, helping developers complete code as they type
- ChatGPT copy-paste workflows: Developers would describe problems to ChatGPT, get code solutions, then manually copy and paste into their editors
- Cursor AI IDE: First AI-powered IDE, fork of VS Code with integrated AI features for code generation and smart rewrites
- GitHub Copilot Chat: Major advancement - AI now aware of open files and context, could copy snippets directly from chat into editor
- Windsurf IDE: Agentic IDE with deep codebase understanding and real-time awareness of developer actions
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

.timeline-container {
  position: relative;
  max-width: 900px;
  margin: 0 auto;
  padding: 10px 40px;
  height: 400px;
  overflow: visible;
}

.timeline-container::before {
  content: '';
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 3px;
  background: linear-gradient(180deg, #4EC5D4 0%, #146b8c 50%, #4EC5D4 100%);
  transform: translateX(-50%);
}

.timeline-item {
  position: relative;
  margin: 12px 0;
  display: flex;
  align-items: center;
  min-height: 45px;
}

.timeline-item:nth-child(odd) {
  flex-direction: row;
  justify-content: flex-start;
}

.timeline-item:nth-child(even) {
  flex-direction: row-reverse;
  justify-content: flex-start;
}

.timeline-item:nth-child(odd) .timeline-content {
  margin-right: auto;
  width: 42%;
  text-align: right;
}

.timeline-item:nth-child(even) .timeline-content {
  margin-left: auto;
  width: 42%;
  text-align: left;
}

.timeline-dot {
  width: 14px;
  height: 14px;
  border-radius: 50%;
  background: #4EC5D4;
  border: 3px solid #146b8c;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  z-index: 10;
  flex-shrink: 0;
}

.timeline-dot.highlight {
  background: #ffd700;
  border-color: #ff6b35;
  box-shadow: 0 0 15px rgba(255, 215, 0, 0.5);
}

.timeline-content {
  background: rgba(255, 255, 255, 0.1);
  padding: 10px 15px;
  border-radius: 8px;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(78, 197, 212, 0.3);
}

.timeline-content h3 {
  margin: 0 0 4px 0;
  font-size: 0.95em;
  font-weight: bold;
  color: #4EC5D4;
}

.timeline-content p {
  margin: 0;
  font-size: 0.8em;
  opacity: 0.9;
  line-height: 1.2;
}

.timeline-item:last-child .timeline-content {
  border-left-color: #ffd700;
}
</style>

<!--
Here is another comment.
-->

---
transition: slide-up
---

# History - 2025

<div class="timeline-container timeline-continued">
  <div class="timeline-item" v-click>
    <div class="timeline-dot"></div>
    <div class="timeline-content">
      <h3>May 2025</h3>
      <p>Claude Code GA launch</p>
    </div>
  </div>
  
  <div class="timeline-item" v-click>
    <div class="timeline-dot"></div>
    <div class="timeline-content">
      <h3>May 2025</h3>
      <p>Amp GA launch</p>
    </div>
  </div>
  
  <div class="timeline-item" v-click>
    <div class="timeline-dot"></div>
    <div class="timeline-content">
      <h3>June 2025</h3>
      <p>MCP servers</p>
    </div>
  </div>
</div>


<!--
Speaker Notes:
- Claude Code GA launch: Anthropic's agentic command line tool launched at "Code with Claude" developer conference on May 22, 2025, transitioning from research preview to general availability with SDK and GitHub integrations
- Amp GA launch: Advanced AI development platform for enhanced coding workflows
- MCP servers: Model Context Protocol servers provide standardized interfaces for AI models to access external tools and data sources, enabling more powerful and extensible AI applications
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

.timeline-container {
  position: relative;
  max-width: 900px;
  margin: 0 auto;
  padding: 10px 40px;
  height: 400px;
  overflow: visible;
}

.timeline-container::before {
  content: '';
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 3px;
  background: linear-gradient(180deg, #4EC5D4 0%, #146b8c 50%, #4EC5D4 100%);
  transform: translateX(-50%);
}

.timeline-item {
  position: relative;
  margin: 12px 0;
  display: flex;
  align-items: center;
  min-height: 45px;
}

.timeline-item:nth-child(odd) {
  flex-direction: row-reverse;
  justify-content: flex-start;
}

.timeline-item:nth-child(even) {
  flex-direction: row;
  justify-content: flex-start;
}

.timeline-item:nth-child(odd) .timeline-content {
  margin-left: auto;
  width: 42%;
  text-align: left;
}

.timeline-item:nth-child(even) .timeline-content {
  margin-right: auto;
  width: 42%;
  text-align: right;
}

.timeline-dot {
  width: 14px;
  height: 14px;
  border-radius: 50%;
  background: #4EC5D4;
  border: 3px solid #146b8c;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  z-index: 10;
  flex-shrink: 0;
}

.timeline-dot.highlight {
  background: #ffd700;
  border-color: #ff6b35;
  box-shadow: 0 0 15px rgba(255, 215, 0, 0.5);
}

.timeline-content {
  background: rgba(255, 255, 255, 0.1);
  padding: 10px 15px;
  border-radius: 8px;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(78, 197, 212, 0.3);
}

.timeline-content h3 {
  margin: 0 0 4px 0;
  font-size: 0.95em;
  font-weight: bold;
  color: #4EC5D4;
}

.timeline-content p {
  margin: 0;
  font-size: 0.8em;
  opacity: 0.9;
  line-height: 1.2;
}

.timeline-item:last-child .timeline-content {
  border-left-color: #ffd700;
}

.timeline-continued::before {
  background: linear-gradient(180deg, #4EC5D4 0%, #146b8c 50%, #4EC5D4 100%);
  top: -20px;
}

.timeline-continued {
  padding-top: 0;
}

.timeline-continued .timeline-item:first-child {
  margin-top: 20px;
}
</style>

---
transition: fade-out
---

# Pair AI Journey

<div class="image-transition-container">
  <div class="image-item first" v-click="1" :class="{ 'active': $slidev.nav.clicks === 1, 'background': $slidev.nav.clicks >= 2 }">
    <img src="/pictures/pairai.png" alt="Pair AI" />
  </div>
  
  <div class="image-item second" v-click="2" :class="{ 'active': $slidev.nav.clicks === 2, 'background': $slidev.nav.clicks >= 3 }">
    <img src="/pictures/pairaianger.png" alt="Pair AI Anger" />
  </div>
  
  <div class="image-item third" v-click="3" :class="{ 'active': $slidev.nav.clicks === 3 }">
    <img src="/pictures/pairaiidea.png" alt="Pair AI Idea" />
  </div>
</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

.image-transition-container {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 400px;
  margin: 3rem auto;
  padding: 2rem;
}

.image-item {
  position: absolute;
  opacity: 0;
  transform: scale(0);
  transition: all 1s ease-in-out;
  z-index: 1;
}

.image-item.active {
  opacity: 1;
  transform: scale(1);
  z-index: 10;
}

.image-item.background {
  opacity: 0.3;
  transform: scale(0.4);
  z-index: 1;
}

.image-item.background.first {
  transform: scale(0.3) translateX(-300px) translateY(-150px);
}

.image-item.background.second {
  transform: scale(0.3) translateX(-150px) translateY(-150px);
}

.image-item img {
  max-height: 450px;
  max-width: 600px;
  object-fit: contain;
  border-radius: 12px;
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(78, 197, 212, 0.3);
}

</style>

<!--
Speaker Notes:

The Pair AI Journey - A Story of Evolution

**First Image**: When developers first start pair programming with AI agents, there's this incredible excitement and amazement. You see what these tools can do - they understand your code, they suggest solutions, they can write entire functions. It feels like magic. Both developer and AI are working together harmoniously, and you think "This is the future!"

**Second Image**: But then reality hits. Things start going wrong. The AI makes mistakes, suggests buggy code, doesn't understand your specific context or constraints. It keeps suggesting the same wrong approach over and over. You spend more time correcting the AI than writing code yourself. Frustration builds. The AI that seemed so promising now feels like it's fighting against you rather than helping.

**Third Image**: And here we are at the turning point. This is where the community splits. Some people throw up their hands and say "See? I told you so. This AI stuff is crap. It doesn't work. It's definitely not taking my job." But others - the ones with the lightbulb moment - they start thinking differently. They ask: "How can we improve this interaction? How can we give the AI more help? How can we design better workflows?" These are the people who understand that the problem isn't the technology itself, but how we're using it. They're the ones who will figure out how to make AI pair programming truly effective.
-->

---
transition: slide-up
level: 2
layout: center
class: text-center
---

# Disclaimer

<div class="disclaimer-content">
  <div class="soft-language" v-click>
    <span class="highlight">can influence</span> • <span class="highlight">may affect</span> • <span class="highlight">might lead to</span>
  </div>
  
  <div class="soft-language" v-click>
    <span class="highlight">could result in</span> • <span class="highlight">has the potential to</span> • <span class="highlight">is correlated with</span>
  </div>
  
  <div class="soft-language" v-click>
    <span class="highlight">seems to</span> • <span class="highlight">appears to</span> • <span class="highlight">tends to</span>
  </div>
  
  <div class="soft-language" v-click>
    <span class="highlight">is likely to</span> • <span class="highlight">is often observed to</span> • <span class="highlight">in some cases</span>
  </div>
  
  <div class="soft-language" v-click>
    <span class="highlight">reportedly</span>
  </div>
  
  <p v-click class="disclaimer-note">
    <em>All sources use very soft language - there are not many hard facts</em>
  </p>
</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  margin-bottom: 2rem;
}

.disclaimer-content {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
}

.soft-language {
  font-size: 1.2em;
  margin: 1rem 0;
  line-height: 1.8;
}

.highlight {
  color: #4EC5D4;
  font-weight: 600;
  padding: 0.2rem 0.4rem;
  background: rgba(78, 197, 212, 0.1);
  border-radius: 4px;
  margin: 0 0.2rem;
}

.disclaimer-note {
  margin-top: 2rem;
  font-size: 1.1em;
  color: #888;
  font-style: italic;
  padding: 1rem;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 8px;
  border-left: 4px solid #4EC5D4;
}
</style>

---
layout: center
class: text-center
---

# 2nd Disclaimer: It Depends

<div class="depends-content">
  <div class="depends-item" v-click>
    <h3>Which model you ask</h3>
    <p>Using smaller models to demonstrate some of the shortcomings</p>
  </div>
  
  <div class="depends-item" v-click>
    <h3>Through which interface you ask</h3>
  </div>
  
  <div class="depends-item" v-click>
    <h3>What it already knows about you</h3>
    <p>(ChatGPT memory)</p>
  </div>
  
  <div class="depends-item" v-click>
    <h3>How often you ask</h3>
  </div>
  
  <div class="depends-item" v-click>
    <h3>When you ask</h3>
    <p>(how many "r" in strawberry)</p>
  </div>
</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  margin-bottom: 2rem;
}

.depends-content {
  max-width: 700px;
  margin: 0 auto;
  padding: 2rem;
}

.depends-item {
  margin: 2rem 0;
  padding: 1.5rem;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
}

.depends-item h3 {
  color: #4EC5D4;
  font-size: 1.3em;
  margin: 0 0 0.5rem 0;
  font-weight: 600;
}

.depends-item p {
  color: #888;
  font-size: 1em;
  margin: 0;
  font-style: italic;
}
</style>

---

# Kent Beck Skills

<div class="centered-image">
  <img src="/pictures/kent-beck-skills.png" alt="Kent Beck Skills" />
</div>

<style>
.centered-image {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 400px;
  margin: 2rem auto;
}

.centered-image img {
  max-height: 100%;
  max-width: 100%;
  object-fit: contain;
  border-radius: 8px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}
</style>

---

