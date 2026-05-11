# Contributing to AI Control Center

## Adding a New Tool Card

When adding a new tool to `ai-control-center.html`, **insert the card in alphabetical order by tool name**.

### Steps

1. Find the correct alphabetical position in the `<div class="grid">` section.
2. Copy an existing `<!-- ToolName -->` + `<div class="card">...</div>` block as a template.
3. Insert your new card between the two cards it falls between alphabetically.
4. Update the README.md tools table, also in alphabetical order.

### Current order (for reference)

1. ChatGPT / Codex
2. Claude
3. DeepSeek
4. Gemini
5. Google AI Studio
6. Grok
7. Groq
8. Kilo Code
9. Kiro
10. MiniMax
11. NotebookLM
12. Ollama
13. OpenCode
14. OpenRouter

> Alphabetical sorting ignores case. For names starting with the same word (e.g. "Open..."), sort by the full name: OpenCode before OpenRouter.

### Card template

```html
<!-- ToolName -->
<div class="card">
  <div class="card-header">
    <div class="card-icon" style="background:#1a1a2a;color:#HEXCOLOR;">X</div>
    <div>
      <div class="card-title">Tool Name</div>
      <div class="card-subtitle">Provider · domain.com</div>
    </div>
  </div>
  <div>
    <div class="section-label">Web</div>
    <a class="launch-btn" href="https://..." target="_blank">&#127760; Open Tool</a>
  </div>
  <div>
    <div class="section-label">CLI Commands</div>
    <!-- Use <div class="cli-block"> for commands, or <span class="no-cli"> if none -->
    <div class="cli-block"><code>toolname</code><button class="copy-btn" onclick="copyCmd(this,'toolname')">Copy</button></div>
  </div>
  <div>
    <div class="section-label">IDE Support</div>
    <div class="ide-list">
      <span class="ide-badge">VS Code</span>
    </div>
  </div>
  <div>
    <div class="section-label">Subscription</div>
    <div class="sub-row">
      <input class="sub-input" type="text" placeholder="e.g. Free / Pro · $X/mo">
      <input class="expiry-input" type="date">
      <span class="expiry-badge"></span>
    </div>
  </div>
  <div>
    <div class="section-label">Notes / Reminders</div>
    <textarea class="notes-field" placeholder="e.g. API key, tips..."></textarea>
  </div>
</div>
```

No build step required — just open `ai-control-center.html` in a browser to verify your changes.
