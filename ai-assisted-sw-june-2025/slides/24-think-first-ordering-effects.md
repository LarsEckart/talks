---

# Think first! / Ordering Effects

<div class="ordering-content">
  <div class="ordering-point" v-click>
    <div class="point-bullet">•</div>
    <p>Claude is sometimes sensitive to ordering. This example is on the frontier of Claude's ability to understand nuanced text, and when we swap the order of the arguments from the previous example so that negative is first and positive is second, this changes Claude's overall assessment to positive.</p>
  </div>

  <div class="ordering-point" v-click>
    <div class="point-bullet">•</div>
    <p>In most situations (but not all, confusingly enough), Claude is more likely to choose the second of two options, possibly because in its training data from the web, second options were more likely to be correct.</p>
  </div>
</div>

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 3rem;
  text-align: center;
  font-size: 2.2em;
}

.ordering-content {
  max-width: 900px;
  margin: 0 auto;
  padding: 1rem 2rem;
}

.ordering-point {
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

.ordering-point:hover {
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

.ordering-point p {
  color: #657b83;
  font-size: 1.1em;
  line-height: 1.4;
  margin: 0;
  text-shadow: 0 2px 4px rgba(88, 110, 117, 0.3);
}
</style>