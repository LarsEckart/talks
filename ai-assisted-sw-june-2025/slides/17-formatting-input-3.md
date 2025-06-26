---

# Formatting Input (2/2)

<div class="formatting-content">

  <div class="transition-section" v-click>
    <h3>End of your prompt should firmly transition from explaining to solving the problem</h3>
    <p>As simple as including a question mark at the end</p>
  </div>

  <div class="remember-section" v-click>
    <h3>Remember:</h3>
    <p>LLMs read through your prompt once, from beginning to end.</p>
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

.transition-section, .remember-section {
  margin-bottom: 3rem;
  padding: 2rem;
  background: rgba(38, 139, 210, 0.15);
  border-radius: 12px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
}

.transition-section h3, .remember-section h3 {
  color: #2aa198;
  font-size: 1.4em;
  margin: 0 0 0.8rem 0;
  font-weight: 600;
  text-shadow: 0 2px 4px rgba(88, 110, 117, 0.3);
}

.transition-section p, .remember-section p {
  color: #657b83;
  font-size: 1.2em;
  margin: 0;
  line-height: 1.5;
  text-shadow: 0 2px 4px rgba(88, 110, 117, 0.3);
}

.remember-section {
  background: rgba(42, 161, 152, 0.2);
  border-left-color: #2aa198;
}
</style>