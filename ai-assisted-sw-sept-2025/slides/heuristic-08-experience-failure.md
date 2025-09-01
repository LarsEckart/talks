---
layout: image-right
image: https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.0.3
---

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 2rem;
}

.centered-image {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: auto;
}

.centered-image img {
  border-radius: 8px;
  box-shadow: 0 8px 32px rgba(88, 110, 117, 0.3);
  max-width: 100%;
  height: auto;
}
</style>

# Make the agents experience the failure

<v-click>

**Don't just copy-paste errors**

</v-click>

<v-click>

- Have it run the app/tests itself
- Let it see the failures firsthand
- Creates a feedback loop: try → see result → adjust
- The agents "learn" from direct experience

</v-click>

<v-click>

**Direct experience > secondhand descriptions (but both work)**

</v-click>

<!--
This heuristic leverages Claude's ability to directly interact with your development environment. Rather than being a middleman describing errors, let Claude discover and experience them directly.

This creates a more natural debugging cycle where Claude can iterate quickly - make a change, run a test, see the result, adjust accordingly. It's closer to how human developers work and often leads to faster resolution.

While copying errors still has its place, giving Claude the tools to experience problems firsthand often produces better debugging outcomes.
-->
