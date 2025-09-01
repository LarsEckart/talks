---
transition: fade-out
---

# Pair AI Journey

<div class="image-transition-container">
  <div class="image-item first" v-click="1" :class="{ 'active': $slidev.nav.clicks === 1, 'background': $slidev.nav.clicks >= 2 }">
    <img src="/pairai.png" alt="Pair AI" />
  </div>

  <div class="image-item second" v-click="2" :class="{ 'active': $slidev.nav.clicks === 2, 'background': $slidev.nav.clicks >= 3 }">
    <img src="/pairaianger.png" alt="Pair AI Anger" />
  </div>

  <div class="image-item third" v-click="3" :class="{ 'active': $slidev.nav.clicks === 3 }">
    <img src="/pairaiidea.png" alt="Pair AI Idea" />
  </div>
</div>

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 2rem;
}

.image-transition-container {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 400px;
  margin: 3rem auto;
  padding: 2rem;
}

.image-item {
  position: absolute;
  opacity: 0;
  transform: scale(0);
  transition: all 1s ease-in-out;
  z-index: 1;
}

.image-item.active {
  opacity: 1;
  transform: scale(1);
  z-index: 10;
}

.image-item.background {
  opacity: 0.3;
  transform: scale(0.4);
  z-index: 1;
}

.image-item.background.first {
  transform: scale(0.3) translateX(-300px) translateY(-150px);
}

.image-item.background.second {
  transform: scale(0.3) translateX(-150px) translateY(-150px);
}

.image-item img {
  max-height: 450px;
  max-width: 600px;
  object-fit: contain;
  border-radius: 12px;
  box-shadow: 0 12px 40px rgba(88, 110, 117, 0.4);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(42, 161, 152, 0.3);
}

</style>

<!--
Speaker Notes:

The Pair AI Journey - A Story of Evolution

**First Image**: When developers first start pair programming with AI agents, there's this incredible excitement and amazement. You see what these tools can do - they understand your code, they suggest solutions, they can write entire functions. It feels like magic. Both developer and AI are working together harmoniously, and you think "This is the future!"

**Second Image**: But then reality hits. Things start going wrong. The AI makes mistakes, suggests buggy code, doesn't understand your specific context or constraints. It keeps suggesting the same wrong approach over and over. You spend more time correcting the AI than writing code yourself. Frustration builds. The AI that seemed so promising now feels like it's fighting against you rather than helping.

**Third Image**: And here we are at the turning point. This is where the community splits. Some people throw up their hands and say "See? I told you so. This AI stuff is crap. It doesn't work. It's definitely not taking my job." But others - the ones with the lightbulb moment - they start thinking differently. They ask: "How can we improve this interaction? How can we give the AI more help? How can we design better workflows?" These are the people who understand that the problem isn't the technology itself, but how we're using it. They're the ones who will figure out how to make AI pair programming truly effective.
-->
