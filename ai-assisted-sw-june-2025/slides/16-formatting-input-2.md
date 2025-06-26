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

.instruction-section, .attention-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: rgba(38, 139, 210, 0.15);
  border-radius: 12px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
}

.instruction-section h3, .attention-section h3 {
  color: #2aa198;
  font-size: 1.4em;
  margin: 0 0 0.5rem 0;
  font-weight: 600;
  text-shadow: 0 2px 4px rgba(88, 110, 117, 0.3);
}

.instruction-section h3:last-child {
  margin: 0.8rem 0 0 0;
}
</style>