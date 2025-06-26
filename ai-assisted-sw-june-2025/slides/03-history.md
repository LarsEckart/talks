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
  color: #2B90B6;
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
  background: linear-gradient(180deg, #2aa198 0%, #268bd2 50%, #2aa198 100%);
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
  background: #2aa198;
  border: 3px solid #268bd2;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  z-index: 10;
  flex-shrink: 0;
}

.timeline-dot.highlight {
  background: #b58900;
  border-color: #cb4b16;
  box-shadow: 0 0 15px rgba(181, 137, 0, 0.5);
}

.timeline-content {
  background: rgba(253, 246, 227, 0.3);
  padding: 10px 15px;
  border-radius: 8px;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(42, 161, 152, 0.3);
}

.timeline-content h3 {
  margin: 0 0 4px 0;
  font-size: 0.95em;
  font-weight: bold;
  color: #2aa198;
}

.timeline-content p {
  margin: 0;
  font-size: 0.8em;
  opacity: 0.9;
  line-height: 1.2;
}

.timeline-item:last-child .timeline-content {
  border-left-color: #b58900;
}
</style>

<!--
Here is another comment.
-->