---
layout: image-right
image: https://images.unsplash.com/photo-1556075798-4825dfaaf498?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.0.3
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

# Commit before prompting



**Working with agents requires version control discipline**





Workflow:
1. Prompt until the code works
2. **Commit**
3. Refactor with the agent or yourself
4. **Commit**
5. Push remotely





**Committing is cheap**



<!--
This heuristic is about risk management when working with AI. Since you can't predict exactly what changes Claude will make, having clean commit points allows you to easily revert if things go wrong.

Frequent commits become even more important with AI assistance because the changes can be more extensive and unpredictable than typical human changes. It's your safety net for experimentation and bold moves.

This discipline also helps with the iterative process - get it working, commit, then improve it, commit again. Each step is reversible.
-->
