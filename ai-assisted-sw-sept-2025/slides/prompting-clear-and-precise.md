---
layout: default
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
  background: rgba(220, 50, 47, 0.1);
  border-left: 4px solid #dc322f;
}

.good-example {
  background: rgba(42, 161, 152, 0.1);
  border-left: 4px solid #2aa198;
}

.label {
  font-weight: bold;
  font-size: 1em;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.bad-example .label {
  color: #dc322f;
}

.good-example .label {
  color: #2aa198;
}

.bad-example p, .good-example p {
  margin: 0.8rem 0 0 0;
  font-size: 1em;
  line-height: 1.4;
}
</style>
