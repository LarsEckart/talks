---
layout: center
class: text-center
---

<h1 class="slide-title">2nd Disclaimer: It Depends</h1>

<div class="slide-content-container">
  <div class="slide-content-item" v-click>
    <h3>Which model you ask</h3>
    <p>Using smaller models to demonstrate some of the shortcomings</p>
  </div>

  <div class="slide-content-item" v-click>
    <h3>Through which interface you ask</h3>
  </div>

  <div class="slide-content-item" v-click>
    <h3>What it already knows about you</h3>
    <p>(ChatGPT memory)</p>
  </div>
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
  margin: 3rem 0 2rem 0;
}

@keyframes gradient {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.slide-content-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
}

.slide-content-item {
  margin-bottom: 2rem;
  padding: 2rem;
  background: rgba(38, 139, 210, 0.15);
  border-radius: 16px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(42, 161, 152, 0.3);
  transition: all 0.3s ease;
  text-align: center;
}

.slide-content-item:hover {
  background: rgba(38, 139, 210, 0.25);
  transform: translateY(-2px);
}

.slide-content-item h3 {
  color: #2aa198;
  font-size: 1.5em;
  margin: 0 0 1rem 0;
  font-weight: 600;
  text-shadow: 0 2px 4px rgba(88, 110, 117, 0.3);
}

.slide-content-item p {
  font-style: italic;
  color: #657b83;
  margin: 0;
  font-size: 1.1em;
}
</style>