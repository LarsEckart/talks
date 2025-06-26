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
  color: #2B90B6;
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
  background: rgba(38, 139, 210, 0.15);
  border-radius: 12px;
  border-left: 4px solid #2B90B6;
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
  border: 1px solid rgba(43, 144, 182, 0.3);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.output-category:hover {
  background: rgba(38, 139, 210, 0.25);
  transform: translateY(-2px);
}

.output-category h3 {
  color: #2B90B6;
  font-size: 1.3em;
  margin: 0 0 1rem 0;
  font-weight: 600;
  text-shadow: none;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.category-icon {
  font-size: 1.2em;
}

.example-text {
  color: #93a1a1;
  font-size: 0.95em;
  line-height: 1.6;
  text-shadow: none;
  font-style: italic;
}
</style>