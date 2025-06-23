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
layout: center
class: text-center
---

# 2nd Disclaimer: It Depends (2/2)

<div class="depends-content">
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
layout: center
class: text-center
---

# Hitting a Moving Target

<div class="centered-image">
  <img src="/pictures/moving-target.png" alt="Moving Target" />
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
layout: center
---

# Where it started

<div class="thinking-content">
  <div class="thinking-point" v-click>
    <div class="point-bullet">•</div>
    <p><strong>LLMs are document completion engines</strong></p>
  </div>
  
  <div class="thinking-point" v-click>
    <div class="point-bullet">•</div>
    <div class="interaction-content">
      <p><strong>General interactions</strong></p>
      <ul class="interaction-list">
        <li>asking questions & getting explanations</li>
        <li>debugging code snippets</li>
        <li>translating Estonian to English</li>
        <li>and brainstorming ideas</li>
      </ul>
    </div>
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
  margin-bottom: 3rem;
  text-align: center;
  font-size: 2.2em;
}

.thinking-content {
  max-width: 900px;
  margin: 0 auto;
  padding: 1rem 2rem;
}

.thinking-point {
  display: flex;
  align-items: flex-start;
  margin: 1.5rem 0;
  padding: 1.5rem;
  background: rgba(20, 107, 140, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
}

.point-bullet {
  color: #4EC5D4;
  font-size: 1.5em;
  font-weight: bold;
  margin-right: 1rem;
  margin-top: 0.2rem;
  flex-shrink: 0;
}

.thinking-point p {
  margin: 0;
  font-size: 1.2em;
  line-height: 1.4;
  color: #ffffff;
}

.interaction-content p {
  margin-bottom: 1rem;
  font-size: 1.2em;
  color: #4EC5D4;
  font-weight: 600;
}

.interaction-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.interaction-list li {
  font-size: 1.1em;
  margin: 0.5rem 0;
  padding-left: 1rem;
  color: #ffffff;
  line-height: 1.4;
}

.interaction-list li:before {
  content: "•";
  color: #4EC5D4;
  font-weight: bold;
  margin-right: 0.5rem;
  margin-left: -1rem;
}
</style>

---
layout: center
---

# Assigning Roles

<div class="role-content">
  <div class="role-image" v-click>
    <img src="/pictures/assign-role.png" alt="Assigning Roles" />
  </div>
  
  <div class="role-points">
    <div class="point-item" v-click>
      <h3>can improve responses</h3>
    </div>
    <div class="point-item" v-click>
      <h3>the more detail, the better</h3>
    </div>
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
  margin-bottom: 1.5rem;
  text-align: center;
  font-size: 2.2em;
}

.role-content {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 3rem;
  max-width: 1000px;
  margin: 0 auto;
  padding: 1rem 2rem;
  height: 400px;
}

.role-image {
  flex: 0 0 auto;
}

.role-image img {
  max-height: 350px;
  max-width: 400px;
  object-fit: contain;
  border-radius: 12px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}

.role-points {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.point-item {
  padding: 1.2rem 1.5rem;
  background: rgba(78, 197, 212, 0.1);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
  text-align: center;
}

.point-item h3 {
  font-size: 1.3em;
  color: #4EC5D4;
  margin: 0;
  font-weight: 600;
}
</style>

---
layout: center
class: text-center
---

<div class="audience-slide">
  <img src="/pictures/audience.png" alt="Audience" />
</div>

<style>
.audience-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100%;
}

.audience-slide img {
  max-height: 80vh;
  max-width: 90vw;
  object-fit: contain;
}
</style>

---

# Prompting: Clear and Precise

<div class="prompting-content">
  
  <div class="principle-section" v-click>
    <h3>Acronyms and technical terms</h3>
    <div class="example-pair">
      <div class="bad-example">
        <span class="label">Bad:</span>
        <p>I'm having DB connection issues. How to fix it?</p>
      </div>
      <div class="good-example">
        <span class="label">Better:</span>
        <p>I am encountering a connection timeout issue while trying to connect to my Oracle database using JDBC. How can I resolve it?</p>
      </div>
    </div>
  </div>

  <div class="principle-section" v-click>
    <h3>Ask for positives instead of negatives</h3>
    <div class="example-pair">
      <div class="bad-example">
        <span class="label">Bad:</span>
        <p>Don't use global variables</p>
      </div>
      <div class="good-example">
        <span class="label">Better:</span>
        <p>Use local variables or dependency injection to manage state</p>
      </div>
    </div>
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
  text-align: center;
  font-size: 2em;
}

.prompting-content {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 2rem;
}

.principle-section {
  margin-bottom: 3rem;
}

.principle-section h3 {
  color: #4EC5D4;
  font-size: 1.3em;
  margin-bottom: 1.5rem;
  font-weight: 600;
}

.example-pair {
  display: flex;
  gap: 2rem;
  align-items: flex-start;
}

.bad-example, .good-example {
  flex: 1;
  padding: 1.5rem;
  border-radius: 8px;
  backdrop-filter: blur(10px);
}

.bad-example {
  background: rgba(255, 107, 107, 0.1);
  border-left: 4px solid #ff6b6b;
}

.good-example {
  background: rgba(78, 197, 212, 0.1);
  border-left: 4px solid #4EC5D4;
}

.label {
  font-weight: bold;
  font-size: 1em;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.bad-example .label {
  color: #ff6b6b;
}

.good-example .label {
  color: #4EC5D4;
}

.bad-example p, .good-example p {
  margin: 0.8rem 0 0 0;
  font-size: 1em;
  line-height: 1.4;
}
</style>

---

# Prompting: Clear and Precise (2/2)

<div class="prompting-content">
  
  <div class="principle-section" v-click>
    <h3>Bolster your command with a reason</h3>
    <div class="example-pair">
      <div class="bad-example">
        <span class="label">Bad:</span>
        <p>Avoid deeply nested conditionals</p>
      </div>
      <div class="good-example">
        <span class="label">Better:</span>
        <p>Avoid deeply nested conditionals to keep the logic readable and maintainable</p>
      </div>
    </div>
  </div>

  <div class="principle-section" v-click>
    <h3>Avoid absolutes</h3>
    <div class="example-pair">
      <div class="bad-example">
        <span class="label">Bad:</span>
        <p>Never use recursion.</p>
      </div>
      <div class="good-example">
        <span class="label">Better:</span>
        <p>Prefer iteration over recursion for performance, unless the recursive solution is more elegant or the depth is small.</p>
      </div>
    </div>
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
  text-align: center;
  font-size: 2em;
}

.prompting-content {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 2rem;
}

.principle-section {
  margin-bottom: 3rem;
}

.principle-section h3 {
  color: #4EC5D4;
  font-size: 1.3em;
  margin-bottom: 1.5rem;
  font-weight: 600;
}

.example-pair {
  display: flex;
  gap: 2rem;
  align-items: flex-start;
}

.bad-example, .good-example {
  flex: 1;
  padding: 1.5rem;
  border-radius: 8px;
  backdrop-filter: blur(10px);
}

.bad-example {
  background: rgba(255, 107, 107, 0.1);
  border-left: 4px solid #ff6b6b;
}

.good-example {
  background: rgba(78, 197, 212, 0.1);
  border-left: 4px solid #4EC5D4;
}

.label {
  font-weight: bold;
  font-size: 1em;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.bad-example .label {
  color: #ff6b6b;
}

.good-example .label {
  color: #4EC5D4;
}

.bad-example p, .good-example p {
  margin: 0.8rem 0 0 0;
  font-size: 1em;
  line-height: 1.4;
}
</style>

---

# Formatting Input

<div class="formatting-content">
  <div class="main-principle" v-click>
    <p>You can help the model understand logical boundaries of your prompt and context data using a combination of <strong>Markdown formatting</strong> and <strong>XML tags</strong></p>
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
  margin-bottom: 3rem;
  text-align: center;
  font-size: 2.2em;
}

.formatting-content {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 300px;
}

.main-principle {
  text-align: center;
  padding: 3rem;
  background: rgba(20, 107, 140, 0.2);
  border-radius: 16px;
  border: 2px solid rgba(78, 197, 212, 0.4);
  backdrop-filter: blur(10px);
}

.main-principle p {
  font-size: 1.4em;
  line-height: 1.6;
  margin: 0;
  color: #ffffff;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.8);
}

.main-principle strong {
  color: #4EC5D4;
  font-weight: 700;
}
</style>

---

# Formatting Input

<div class="formatting-content">
  
  <div class="instruction-section" v-click>
    <h3>Put your instructions at the beginning of the prompt</h3>
    <h3>And at the end as safety net</h3>
  </div>

  <div class="attention-section" v-click>
    <h3>U-shaped attention curve / Valley of Meh</h3>
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
  text-align: center;
  font-size: 2.2em;
}

.formatting-content {
  max-width: 1000px;
  margin: 0 auto;
  padding: 2rem;
}

.instruction-section, .attention-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: rgba(20, 107, 140, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
}

.instruction-section h3, .attention-section h3 {
  color: #4EC5D4;
  font-size: 1.4em;
  margin: 0 0 0.5rem 0;
  font-weight: 600;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
}

.instruction-section h3:last-child {
  margin: 0.8rem 0 0 0;
}
</style>

---

# Formatting Input (2/2)

<div class="formatting-content">

  <div class="transition-section" v-click>
    <h3>End of your prompt should firmly transition from explaining to solving the problem</h3>
    <p>As simple as including a question mark at the end</p>
  </div>

  <div class="remember-section" v-click>
    <h3>Remember:</h3>
    <p>LLMs read through your prompt once, from beginning to end.</p>
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
  text-align: center;
  font-size: 2.2em;
}

.formatting-content {
  max-width: 1000px;
  margin: 0 auto;
  padding: 2rem;
}

.transition-section, .remember-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: rgba(20, 107, 140, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
}

.transition-section h3, .remember-section h3 {
  color: #4EC5D4;
  font-size: 1.4em;
  margin: 0 0 0.8rem 0;
  font-weight: 600;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
}

.transition-section p, .remember-section p {
  color: #ffffff;
  font-size: 1.2em;
  margin: 0;
  line-height: 1.5;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
}

.remember-section {
  background: rgba(78, 197, 212, 0.2);
  border-left-color: #4EC5D4;
}
</style>

---

# Formatting Input (3/3)

<div class="formatting-content">
  
  <div class="fluffy-section" v-click>
    <h3>Reduce "fluffy" and imprecise descriptions</h3>
  </div>

  <div class="example-section" v-click>
    <div class="bad-example">
      <span class="label">Bad:</span>
      <p>The description for this product should be fairly short, a few sentences only, and not too much more.</p>
    </div>
    <div class="good-example">
      <span class="label">Better:</span>
      <p>Use a 3 to 5 sentence paragraph to describe this product.</p>
    </div>
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
  text-align: center;
  font-size: 2.2em;
}

.formatting-content {
  max-width: 1000px;
  margin: 0 auto;
  padding: 2rem;
}

.fluffy-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: rgba(20, 107, 140, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
  text-align: center;
}

.fluffy-section h3 {
  color: #4EC5D4;
  font-size: 1.6em;
  margin: 0;
  font-weight: 600;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
}

.example-section {
  display: flex;
  gap: 2rem;
  align-items: flex-start;
}

.bad-example, .good-example {
  flex: 1;
  padding: 2rem;
  border-radius: 12px;
  backdrop-filter: blur(10px);
}

.bad-example {
  background: rgba(255, 107, 107, 0.15);
  border-left: 4px solid #ff6b6b;
}

.good-example {
  background: rgba(78, 197, 212, 0.15);
  border-left: 4px solid #4EC5D4;
}

.label {
  font-weight: bold;
  font-size: 1.1em;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  display: block;
  margin-bottom: 1rem;
}

.bad-example .label {
  color: #ff6b6b;
}

.good-example .label {
  color: #4EC5D4;
}

.bad-example p, .good-example p {
  color: #ffffff;
  font-size: 1.1em;
  margin: 0;
  line-height: 1.5;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
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

# Vibe Coding

<div class="tweet-slide">
  <img src="/karpathy-tweet-cropped.png" alt="Andrej Karpathy Tweet about Vibe Coding" />
</div>

<style>
.tweet-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 500px;
  width: 100%;
  padding: 2rem;
}

.tweet-slide img {
  max-height: 100%;
  max-width: 100%;
  object-fit: contain;
  border-radius: 12px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}
</style>

---

# Formatting Output

<div class="formatting-content">
  <div class="output-category" v-click>
    <h3><span class="category-icon">📊</span> Table</h3>
    <div class="example-text">
      "Please create a comparison table of..."
    </div>
  </div>
  
  <div class="output-category" v-click>
    <h3><span class="category-icon">📝</span> List</h3>
    <div class="example-text">
      "List the top 5..." • "Create a bulleted list..." • "Enumerate the steps..."
    </div>
  </div>
  
  <div class="output-category" v-click>
    <h3><span class="category-icon">⚙️</span> Markdown / HTML / JSON / CSV</h3>
    <div class="example-text">
      "Format the response as JSON..." • "Return the data in CSV format..."
    </div>
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
  text-align: center;
  font-size: 2.2em;
}

.formatting-content {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

.output-category {
  padding: 1.5rem;
  background: rgba(20, 107, 140, 0.8);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
  border: 1px solid rgba(78, 197, 212, 0.4);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

.output-category:hover {
  background: rgba(20, 107, 140, 0.9);
  transform: translateY(-2px);
}

.output-category h3 {
  color: #4EC5D4;
  font-size: 1.3em;
  margin: 0 0 1rem 0;
  font-weight: 600;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.category-icon {
  font-size: 1.2em;
}

.example-text {
  color: #ffffff;
  font-size: 0.95em;
  line-height: 1.6;
  text-shadow: 0 1px 3px rgba(0, 0, 0, 0.6);
  font-style: italic;
}
</style>

---

# Formatting Output (2/2)

<div class="formatting-content">
  <div class="output-category" v-click>
    <h3><span class="category-icon">📋</span> Text hierarchy</h3>
    <div class="example-text">
      "Organize with clear headings..." • "Use numbered sections..."
    </div>
  </div>
  
  <div class="output-category" v-click>
    <h3><span class="category-icon">🔢</span> LaTeX</h3>
    <div class="example-text">
      "Show the mathematical formula in LaTeX format..."
    </div>
  </div>
  
  <div class="output-category" v-click>
    <h3><span class="category-icon">📈</span> Mermaid</h3>
    <div class="example-text">
      "Create a flowchart diagram..." • "Generate a sequence diagram..."
    </div>
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
  text-align: center;
  font-size: 2.2em;
}

.formatting-content {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

.output-category {
  padding: 1.5rem;
  background: rgba(20, 107, 140, 0.8);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
  border: 1px solid rgba(78, 197, 212, 0.4);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

.output-category:hover {
  background: rgba(20, 107, 140, 0.9);
  transform: translateY(-2px);
}

.output-category h3 {
  color: #4EC5D4;
  font-size: 1.3em;
  margin: 0 0 1rem 0;
  font-weight: 600;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.category-icon {
  font-size: 1.2em;
}

.example-text {
  color: #ffffff;
  font-size: 0.95em;
  line-height: 1.6;
  text-shadow: 0 1px 3px rgba(0, 0, 0, 0.6);
  font-style: italic;
}
</style>

---

# How to trigger Chain of Thought (2/2)

<div class="content-container">
  <div class="content-item" v-click>
    <h4>Follow these steps to find an answer:</h4>
    <ul>
      <li v-click>Define what "fewer bugs in production" means in measurable terms</li>
      <li v-click>Identify typical sources of bugs in OOP and in FP</li>
      <li v-click>Consider how each paradigm mitigates or amplifies those sources</li>
      <li v-click>Compare the outcomes and arrive at a reasoned conclusion</li>
    </ul>
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
  text-align: center;
  font-size: 2.2em;
}

.content-container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 1rem 2rem;
}

.question-section {
  margin: 1.5rem 0;
  padding: 1.5rem;
  background: rgba(78, 197, 212, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
  text-align: center;
}

.question-section h3 {
  color: #4EC5D4;
  font-size: 1.5em;
  margin: 0;
  font-weight: 600;
  line-height: 1.4;
}

.content-item {
  margin: 1.5rem 0;
  padding: 1.5rem;
  background: rgba(20, 107, 140, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
}

.content-item h4 {
  color: #4EC5D4;
  font-size: 1.3em;
  margin: 0;
  font-weight: 600;
  line-height: 1.4;
}

.content-item ul {
  margin: 1rem 0 0 0;
  padding-left: 1.5rem;
}

.content-item li {
  color: #ffffff;
  font-size: 1.1em;
  margin: 0.8rem 0;
  line-height: 1.4;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
}
</style>

---

# Think first! / Chain of Thought

<div class="thinking-content">
  <div class="thinking-point" v-click>
    <div class="point-bullet">•</div>
    <p>Giving LLMs time to think step by step sometimes makes LLMs more accurate, particularly for complex tasks.</p>
  </div>
  
  <div class="thinking-point" v-click>
    <div class="point-bullet">•</div>
    <p>Thinking only counts when it's out loud.</p>
  </div>
  
  <div class="thinking-point" v-click>
    <div class="point-bullet">•</div>
    <p>You cannot ask LLMs to think but output only the answer - in this case, no thinking has actually occurred.</p>
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
  margin-bottom: 3rem;
  text-align: center;
  font-size: 2.2em;
}

.thinking-content {
  max-width: 900px;
  margin: 0 auto;
  padding: 1rem 2rem;
}

.thinking-point {
  display: flex;
  align-items: flex-start;
  margin: 1.5rem 0;
  padding: 1.5rem;
  background: rgba(20, 107, 140, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
}

.thinking-point:hover {
  background: rgba(20, 107, 140, 0.25);
  transform: translateY(-2px);
}

.point-bullet {
  color: #4EC5D4;
  font-size: 1.5em;
  font-weight: bold;
  margin-right: 1.2rem;
  margin-top: 0.1rem;
  flex-shrink: 0;
}

.thinking-point p {
  color: #ffffff;
  font-size: 1.1em;
  line-height: 1.4;
  margin: 0;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
}
</style>

---

# How to trigger Chain of Thought

<div class="content-container">
  <div class="question-section" v-click>
    <h3>Which software development paradigm leads to fewer bugs in production: Object-Oriented Programming (OOP) or Functional Programming (FP)?</h3>
  </div>
  
  <div class="content-item" v-click>
    <h4>Think step by step before arriving at an answer</h4>
  </div>
  
  <div class="content-item" v-click>
    <h4>Explain your rationale before giving an answer</h4>
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
  text-align: center;
  font-size: 2.2em;
}

.content-container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 1rem 2rem;
}

.question-section {
  margin: 1.5rem 0;
  padding: 1.5rem;
  background: rgba(78, 197, 212, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
  text-align: center;
}

.question-section h3 {
  color: #4EC5D4;
  font-size: 1.5em;
  margin: 0;
  font-weight: 600;
  line-height: 1.4;
}

.content-item {
  margin: 1.5rem 0;
  padding: 1.5rem;
  background: rgba(20, 107, 140, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
}

.content-item h4 {
  color: #4EC5D4;
  font-size: 1.3em;
  margin: 0;
  font-weight: 600;
  line-height: 1.4;
}

.content-item ul {
  margin: 1rem 0 0 0;
  padding-left: 1.5rem;
}

.content-item li {
  color: #ffffff;
  font-size: 1.1em;
  margin: 0.8rem 0;
  line-height: 1.4;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
}
</style>

---

# Think first! / Ordering Effects

<div class="ordering-content">
  <div class="ordering-point" v-click>
    <div class="point-bullet">•</div>
    <p>Claude is sometimes sensitive to ordering. This example is on the frontier of Claude's ability to understand nuanced text, and when we swap the order of the arguments from the previous example so that negative is first and positive is second, this changes Claude's overall assessment to positive.</p>
  </div>
  
  <div class="ordering-point" v-click>
    <div class="point-bullet">•</div>
    <p>In most situations (but not all, confusingly enough), Claude is more likely to choose the second of two options, possibly because in its training data from the web, second options were more likely to be correct.</p>
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
  margin-bottom: 3rem;
  text-align: center;
  font-size: 2.2em;
}

.ordering-content {
  max-width: 900px;
  margin: 0 auto;
  padding: 1rem 2rem;
}

.ordering-point {
  display: flex;
  align-items: flex-start;
  margin: 1.5rem 0;
  padding: 1.5rem;
  background: rgba(20, 107, 140, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
}

.ordering-point:hover {
  background: rgba(20, 107, 140, 0.25);
  transform: translateY(-2px);
}

.point-bullet {
  color: #4EC5D4;
  font-size: 1.5em;
  font-weight: bold;
  margin-right: 1.2rem;
  margin-top: 0.1rem;
  flex-shrink: 0;
}

.ordering-point p {
  color: #ffffff;
  font-size: 1.1em;
  line-height: 1.4;
  margin: 0;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.6);
}
</style>

---

# Prompting reasoning models

<div class="reasoning-content">
  
  <div class="model-section" v-click>
    <h3>Reasoning models</h3>
    <ul class="model-points">
      <li>trained to think longer and harder about complex tasks</li>
      <li>execute tasks with high accuracy and precision</li>
      <li>like a senior co-worker. You can give them a goal to achieve and trust them to work out the details.</li>
    </ul>
  </div>

  <div class="model-section" v-click>
    <h3>GPT models</h3>
    <ul class="model-points">
      <li>lower-latency, more cost-efficient</li>
      <li>The workhorses</li>
      <li>like a junior coworker. They'll perform best with explicit instructions to create a specific output.</li>
    </ul>
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
  text-align: center;
  font-size: 2em;
}

.reasoning-content {
  max-width: 900px;
  margin: 0 auto;
  padding: 0 2rem;
}

.model-section {
  margin-bottom: 2.5rem;
  padding: 1.5rem;
  background: rgba(20, 107, 140, 0.15);
  border-radius: 12px;
  border-left: 4px solid #4EC5D4;
  backdrop-filter: blur(10px);
}

.model-section h3 {
  color: #4EC5D4;
  font-size: 1.4em;
  margin-bottom: 1rem;
  font-weight: 600;
}

.model-points {
  margin: 0;
  padding-left: 1.5rem;
  list-style: none;
}

.model-points li {
  color: #ffffff;
  font-size: 1em;
  line-height: 1.4;
  margin: 0.8rem 0;
  position: relative;
}

.model-points li::before {
  content: "•";
  color: #4EC5D4;
  font-size: 1.2em;
  font-weight: bold;
  position: absolute;
  left: -1.2rem;
  top: 0;
}
</style>

---

