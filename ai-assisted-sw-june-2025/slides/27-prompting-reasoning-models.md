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
  color: #2B90B6;
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
  background: rgba(38, 139, 210, 0.15);
  border-radius: 12px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
}

.model-section h3 {
  color: #2aa198;
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
  color: #657b83;
  font-size: 1em;
  line-height: 1.4;
  margin: 0.8rem 0;
  position: relative;
}

.model-points li::before {
  content: "•";
  color: #2aa198;
  font-size: 1.2em;
  font-weight: bold;
  position: absolute;
  left: -1.2rem;
  top: 0;
}
</style>