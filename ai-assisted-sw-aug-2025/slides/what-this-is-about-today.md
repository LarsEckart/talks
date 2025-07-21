
<h1 class="slide-title-gradient">What this is about today</h1>

<div v-click>

### Where we are today

</div>

<div v-click>

### What I want you to know

</div>

<div v-click>

### What I want you to try/experience

</div>

<style>
.slide-title-gradient {
  background: linear-gradient(135deg, #4EC5D4 0%, #146b8c 50%, #4EC5D4 100%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-size: 200% 200%;
  animation: gradient 3s ease infinite;
  margin-bottom: 3rem;
  text-align: center;
  font-size: 2.2em;
  font-weight: 700;
}

@keyframes gradient {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.slidev-page div[v-click] {
  margin-bottom: 2rem;
  padding: 2rem;
  background: rgba(38, 139, 210, 0.15);
  border-radius: 16px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(42, 161, 152, 0.3);
  transition: all 0.3s ease;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

.slidev-page div[v-click]:hover {
  background: rgba(38, 139, 210, 0.25);
  transform: translateY(-2px);
}

h3 {
  color: #2aa198;
  font-size: 1.5em;
  margin: 0;
  font-weight: 600;
  text-align: center;
  text-shadow: 0 2px 4px rgba(88, 110, 117, 0.3);
}
</style>