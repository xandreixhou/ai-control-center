# AI Tools Reference

Detailed documentation for each AI tool included in the Control Center.

---

## Claude

- **Provider:** Anthropic
- **Web:** https://claude.ai
- **CLI:** Yes — via Kiro CLI or the `claude` command
- **CLI Commands:**
  ```
  claude
  claude --help
  ```
- **IDE Support:**
  - Kiro — native, built-in
  - Cursor — native, built-in
  - VS Code — via extension
  - Visual Studio — via extension
  - Antigravity — supported
- **API:** https://console.anthropic.com
- **Notes:** Strong at reasoning, coding, and long-context tasks. Used natively by Kiro CLI.

---

## ChatGPT / OpenAI Codex

- **Provider:** OpenAI
- **Web:** https://chatgpt.com
- **CLI:** Yes — via `codex` (OpenAI Codex CLI)
- **CLI Commands:**
  ```
  codex
  codex --help
  ```
- **IDE Support:**
  - Cursor — native, built-in
  - VS Code — via GitHub Copilot extension
  - Visual Studio — via extension
  - Antigravity — supported
  - Kiro — via API key
- **API:** https://platform.openai.com
- **Notes:** GPT-4o is the default model. Codex CLI is a separate tool for agentic coding tasks.

---

## Gemini

- **Provider:** Google
- **Web:** https://gemini.google.com
- **CLI:** Yes — via `gemini` CLI
- **CLI Commands:**
  ```
  gemini
  gemini --help
  ```
- **IDE Support:**
  - VS Code — via Gemini Code Assist extension
  - Cursor — supported
  - Visual Studio — via extension
  - Antigravity — supported
  - Kiro — via API key
- **API:** https://aistudio.google.com
- **Notes:** Gemini 2.0 Flash and Pro are the current flagship models. Strong multimodal capabilities.

---

## Grok

- **Provider:** xAI
- **Web:** https://grok.com
- **CLI:** No official CLI — API access only
- **CLI Commands:** None (use OpenRouter or direct API calls)
- **IDE Support:**
  - VS Code — via API key configuration
  - Cursor — via API key configuration
  - Antigravity — supported
  - Kiro — via API key
- **API:** https://console.x.ai
- **Notes:** Available via X (Twitter) Premium or direct API. Also accessible through OpenRouter.

---

## NotebookLM

- **Provider:** Google
- **Web:** https://notebooklm.google.com
- **CLI:** None
- **IDE Support:** None
- **Notes:** Best used for research, summarization, and Q&A over uploaded documents. Supports PDFs, Google Docs, YouTube links, and more. No API or CLI available as of 2026.

---

## MiniMax

- **Provider:** MiniMax AI
- **Web:** https://www.minimaxi.com
- **CLI:** No official CLI — API access only
- **CLI Commands:** None (use direct API calls)
- **IDE Support:**
  - VS Code — via API key configuration
  - Cursor — via API key configuration
  - Kiro — via API key
- **API:** https://www.minimaxi.com/platform
- **Notes:** Supports text, image, video, and audio generation. Strong multilingual capabilities.

---

## OpenRouter

- **Provider:** OpenRouter
- **Web:** https://openrouter.ai
- **CLI:** Via `curl` or any HTTP client
- **CLI Commands:**
  ```
  curl https://openrouter.ai/api/v1/chat/completions \
    -H "Authorization: Bearer YOUR_API_KEY" \
    -H "Content-Type: application/json" \
    -d '{"model":"openai/gpt-4o","messages":[{"role":"user","content":"Hello"}]}'
  ```
- **IDE Support:**
  - VS Code — via API key configuration
  - Cursor — via API key configuration
  - Kiro — via API key
  - Antigravity — supported
- **API:** https://openrouter.ai/keys
- **Notes:** Acts as a unified gateway to 100+ models (GPT-4o, Claude, Gemini, Grok, Llama, etc.) under a single API key. Great for switching models without changing code.

---

## Kiro

- **Provider:** AWS / Amazon
- **Web:** https://kiro.dev
- **CLI:** Yes — `kiro` command
- **CLI Commands:**
  ```
  kiro
  kiro chat
  kiro --help
  ```
- **IDE Support:**
  - Kiro IDE — native
  - VS Code — via extension
  - Cursor — supported
  - Visual Studio — supported
  - Antigravity — supported
- **Notes:** AI-powered development agent. Runs in the terminal or as an IDE. Powered by Claude under the hood.

---

## Ollama

- **Provider:** Ollama (open source)
- **Web:** https://ollama.com
- **CLI:** Yes — `ollama` command
- **CLI Commands:**
  ```
  ollama serve              # Start the local API server (port 11434)
  ollama run llama3         # Run a model interactively
  ollama run mistral        # Run Mistral
  ollama run codellama      # Run CodeLlama for coding tasks
  ollama list               # List installed models
  ollama pull <model>       # Download a model
  ollama rm <model>         # Remove a model
  ollama ps                 # Show running models
  ```
- **IDE Support:**
  - VS Code — via Continue extension (set base URL to http://localhost:11434)
  - Cursor — via local API configuration
  - Visual Studio — via extension
  - Kiro — via local API key configuration
  - Antigravity — supported
- **Local API:** http://localhost:11434
- **Notes:** Runs LLMs fully locally — no internet required after model download. Popular models: llama3, mistral, codellama, phi3, gemma. Free and private.
