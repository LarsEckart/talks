---

# Formatting Input (3/3)

<div class="formatting-content">

  <div class="principle-section" v-click>
    <h3>Reduce "fluffy" and imprecise descriptions</h3>
  </div>

  <div class="comparison-section" v-click>
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
  color: #2B90B6;
  margin-bottom: 2rem;
  text-align: center;
  font-size: 2.2em;
}

.formatting-content {
  max-width: 1000px;
  margin: 0 auto;
  padding: 2rem;
}

.principle-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: rgba(38, 139, 210, 0.15);
  border-radius: 12px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
  text-align: center;
}

.principle-section h3 {
  color: #2aa198;
  font-size: 1.6em;
  margin: 0;
  font-weight: 600;
  text-shadow: 0 2px 4px rgba(88, 110, 117, 0.3);
}

.comparison-section {
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
  background: rgba(220, 50, 47, 0.15);
  border-left: 4px solid #dc322f;
}

.good-example {
  background: rgba(42, 161, 152, 0.15);
  border-left: 4px solid #2aa198;
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
  color: #dc322f;
}

.good-example .label {
  color: #2aa198;
}

.bad-example p, .good-example p {
  color: #657b83;
  font-size: 1.1em;
  margin: 0;
  line-height: 1.5;
  text-shadow: 0 2px 4px rgba(88, 110, 117, 0.3);
}
</style>