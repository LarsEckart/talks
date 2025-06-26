---

# Zero-Shot vs One-Shot Prompting

<div class="prompting-content">

  <div class="principle-section" v-click>
    <h3>Zero-Shot Prompting</h3>
    <div class="example-container">
      <div class="definition">
        <span class="label">Definition:</span>
        <p>Asking the AI to perform a task without providing any examples</p>
      </div>
      <div class="example">
        <span class="label">Example:</span>
        <p><strong>Prompt:</strong> "Classify the sentiment of this text: 'I love this new phone!'"</p>
        <p><strong>Response:</strong> "Positive"</p>
      </div>
    </div>
  </div>

</div>

<style>
h1 {
  color: #2B90B6;
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
  color: #2aa198;
  font-size: 1.3em;
  margin-bottom: 1.5rem;
  font-weight: 600;
}

.example-container {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.definition, .example {
  padding: 1.5rem;
  border-radius: 8px;
  backdrop-filter: blur(10px);
}

.definition {
  background: rgba(42, 161, 152, 0.1);
  border-left: 4px solid #2aa198;
}

.example {
  background: rgba(38, 139, 210, 0.15);
  border-left: 4px solid #268bd2;
}

.label {
  font-weight: bold;
  font-size: 1em;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  color: #2aa198;
}

.definition p, .example p {
  margin: 0.5rem 0;
  color: #657b83;
  line-height: 1.4;
}

.example em {
  color: #839496;
  font-style: italic;
}

.example strong {
  color: #2aa198;
}
</style>