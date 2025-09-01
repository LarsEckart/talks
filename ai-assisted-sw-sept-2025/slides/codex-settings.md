---
layout: default
---

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 2rem;
}
</style>

# Codex


## Approval Modes

| Mode | What's Auto-approved | Requires Approval |
|------|---------------------|-------------------|
| **Suggest** (default) | • Read any file in the repo | • All file writes/patches<br>• All shell commands |
| **Auto-Edit** | • Read files<br>• Write/patch files | • All shell commands |
| **Full Auto** | • Read files<br>• Write files<br>• Execute shell commands | (Nothing) |

<!--
Speaker Notes:
- Explain the progression from restrictive to permissive modes
- Suggest mode is safest but requires constant approval
- Full Auto mode gives maximum productivity but requires trust in the AI
- Consider your team's comfort level and security requirements
-->
