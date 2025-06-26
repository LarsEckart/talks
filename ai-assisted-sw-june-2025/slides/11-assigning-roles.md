---
layout: center
---

# Assigning Roles

<div class="role-content">
  <div class="role-image" v-click>
    <img src="/pictures/assign-role.png" alt="Assigning Roles" />
  </div>

  <div class="role-points">
    <div class="point-item" v-click>
      <h3>can improve responses</h3>
    </div>
    <div class="point-item" v-click>
      <h3>the more detail, the better</h3>
    </div>
  </div>
</div>

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 1.5rem;
  text-align: center;
  font-size: 2.2em;
}

.role-content {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 3rem;
  max-width: 1000px;
  margin: 0 auto;
  padding: 1rem 2rem;
  height: 400px;
}

.role-image {
  flex: 0 0 auto;
}

.role-image img {
  max-height: 350px;
  max-width: 400px;
  object-fit: contain;
  border-radius: 12px;
  box-shadow: 0 8px 32px rgba(88, 110, 117, 0.3);
}

.role-points {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.point-item {
  padding: 1.2rem 1.5rem;
  background: rgba(42, 161, 152, 0.1);
  border-radius: 12px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
  text-align: center;
}

.point-item h3 {
  font-size: 1.3em;
  color: #2aa198;
  margin: 0;
  font-weight: 600;
}
</style>