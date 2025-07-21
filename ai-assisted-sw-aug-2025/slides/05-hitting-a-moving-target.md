---
layout: center
class: text-center
---

<h1 class="slide-title">Hitting a Moving Target</h1>

<div class="slide-image-center">
  <img src="/moving-target.png" alt="Moving Target" />
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

.slide-image-center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: auto;
  padding: 2rem;
}

.slide-image-center img {
  max-width: 80%;
  max-height: 70vh;
  object-fit: contain;
  border-radius: 12px;
  box-shadow: 0 12px 40px rgba(88, 110, 117, 0.4);
}
</style>