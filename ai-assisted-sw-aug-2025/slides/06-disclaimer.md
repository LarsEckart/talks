---
transition: fade-out
level: 2
layout: center
class: text-center
---

<h1 class="slide-title">Disclaimer</h1>

<div class="slide-content-container-wide">
  <div class="soft-language" v-click>
    <span class="highlight">can influence</span> • <span class="highlight">may affect</span> • <span class="highlight">might lead to</span>
  </div>

  <div class="soft-language" v-click>
    <span class="highlight">could result in</span> • <span class="highlight">has the potential to</span> • <span class="highlight">is correlated with</span>
  </div>

  <div class="soft-language" v-click>
    <span class="highlight">seems to</span> • <span class="highlight">appears to</span> • <span class="highlight">tends to</span>
  </div>

  <div class="soft-language" v-click>
    <span class="highlight">is likely to</span> • <span class="highlight">is often observed to</span> • <span class="highlight">in some cases</span>
  </div>

  <div class="soft-language" v-click>
    <span class="highlight">reportedly</span>
  </div>

  <p v-click class="disclaimer-note">
    <em>All sources use very soft language - there are not many hard facts</em>
  </p>
</div>

<style>
.slide-title {
  background: linear-gradient(135deg, #4EC5D4 0%, #146b8c 50%, #4EC5D4 100%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-size: 200% 200%;
  animation: gradient 3s ease infinite;
  font-size: 2.5em;
  font-weight: 700;
  text-align: center;
  margin-bottom: 2rem;
}

@keyframes gradient {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.slide-content-container-wide {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem;
  text-align: center;
}

.soft-language {
  font-size: 1.2em;
  margin: 1rem 0;
  line-height: 1.8;
}

.highlight {
  color: #2aa198;
  font-weight: 600;
  padding: 0.2rem 0.4rem;
  background: rgba(42, 161, 152, 0.1);
  border-radius: 4px;
  margin: 0 0.2rem;
}

.disclaimer-note {
  margin-top: 2rem;
  font-size: 1.1em;
  color: #93a1a1;
  font-style: italic;
  padding: 1rem;
  background: rgba(253, 246, 227, 0.2);
  border-radius: 8px;
  border-left: 4px solid #2aa198;
}
</style>