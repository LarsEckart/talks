---
layout: default
---

# System Prompt and User Prompt

<div class="content-container">

  <div class="section-item" v-click>
    <h3>System Prompt</h3>
    <ul class="bullet-list">
      <li>Instructions provided by application developer</li>
      <li>Comes first, gets more attention</li>
      <li>Instruction hierarchy, model is trained to prioritize privileged instructions</li>
    </ul>
  </div>

  <div class="section-item" v-click>
    <h3>User Experience</h3>
    <ul class="bullet-list">
      <li>Usually not visible/editable by users</li>
      <li>Both get combined into 1 query to the model</li>
      <li><a href="https://github.com/asgeirtj/system_prompts_leaks" target="_blank">https://github.com/asgeirtj/system_prompts_leaks</a></li>
    </ul>
  </div>

</div>

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 2rem;
  text-align: center;
  font-size: 2em;
}

.content-container {
  max-width: 900px;
  margin: 0 auto;
  padding: 0 2rem;
}

.section-item {
  margin-bottom: 2.5rem;
  padding: 1.5rem;
  background: rgba(38, 139, 210, 0.15);
  border-radius: 12px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
}

.section-item h3 {
  color: #2aa198;
  font-size: 1.4em;
  margin-bottom: 1rem;
  font-weight: 600;
}

.bullet-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.bullet-list li {
  color: #657b83;
  font-size: 1em;
  line-height: 1.4;
  margin-bottom: 0.8rem;
  padding-left: 1.5rem;
  position: relative;
  text-shadow: 0 1px 3px rgba(88, 110, 117, 0.3);
}

.bullet-list li::before {
  content: "•";
  color: #2aa198;
  font-size: 1.2em;
  font-weight: bold;
  position: absolute;
  left: 0;
  top: 0;
}

.bullet-list li:last-child {
  margin-bottom: 0;
}

.bullet-list a {
  color: #2aa198;
  text-decoration: underline;
}

.bullet-list a:hover {
  color: #657b83;
}
</style>
