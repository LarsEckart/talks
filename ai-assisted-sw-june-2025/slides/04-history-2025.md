---
transition: fade-out
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

.timeline-continued::before {
  background: linear-gradient(180deg, #2aa198 0%, #268bd2 50%, #2aa198 100%);
  top: -20px;
}

.timeline-continued {
  padding-top: 0;
}

.timeline-continued .timeline-item:first-child {
  margin-top: 20px;
}
</style>