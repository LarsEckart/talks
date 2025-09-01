---
layout: default
---

# Minimal AI Application Architecture

<div class="diagram-container">

```mermaid
graph LR
    A[😊 User] -->|Query| B[🤖 Model API]
    B -->|Response| A

    subgraph API [" "]
        B
        C[Generation<br/>Processing]
        B -.-> C
    end

    classDef userStyle fill:#2aa198,stroke:#268bd2,stroke-width:3px,color:#586e75
    classDef apiStyle fill:#268bd2,stroke:#2aa198,stroke-width:3px,color:#fdf6e3
    classDef genStyle fill:#268bd2,stroke:#2aa198,stroke-width:2px,color:#fdf6e3

    class A userStyle
    class B apiStyle
    class C genStyle
```

</div>

<div class="caption" v-click>
  <em>The simplest architecture for running an AI application</em>
</div>

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 3rem;
  text-align: center;
  font-size: 2em;
}

.diagram-container {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.diagram-container .mermaid {
  background: rgba(38, 139, 210, 0.05);
  border-radius: 12px;
  padding: 2rem;
  border: 2px solid rgba(42, 161, 152, 0.3);
}

.caption {
  text-align: center;
  margin-top: 2rem;
  font-size: 1.2em;
  color: #2aa198;
  font-style: italic;
}
</style>
