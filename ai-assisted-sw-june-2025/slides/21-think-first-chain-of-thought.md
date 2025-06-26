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
  color: #2B90B6;
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
  background: rgba(38, 139, 210, 0.15);
  border-radius: 12px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
}

.thinking-point:hover {
  background: rgba(38, 139, 210, 0.25);
  transform: translateY(-2px);
}

.point-bullet {
  color: #2aa198;
  font-size: 1.5em;
  font-weight: bold;
  margin-right: 1.2rem;
  margin-top: 0.1rem;
  flex-shrink: 0;
}

.thinking-point p {
  color: #657b83;
  font-size: 1.1em;
  line-height: 1.4;
  margin: 0;
  text-shadow: 0 2px 4px rgba(88, 110, 117, 0.3);
}
</style>