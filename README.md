# AI Control Center

A single-file, browser-based dashboard that centralizes access to all your AI tools — CLI commands, web launchers, IDE compatibility, and personal notes — in one place.

## Overview

Managing multiple AI tools across different interfaces (CLI, web, IDE) can get disorganized fast. This project solves that with a zero-dependency HTML file you can open in any browser, no server or install required.

## Features

- **Web launchers** — one-click buttons to open each AI tool's web interface
- **CLI command reference** — copy-to-clipboard commands for terminal-based tools
- **IDE compatibility** — shows which IDEs support each tool and how
- **Persistent notes** — per-tool notes saved automatically in browser localStorage
- **Professional dark blue theme** — clean, readable, distraction-free

## Tools Included

| Tool | Web | CLI | IDE Support |
|---|---|---|---|
| ChatGPT / Codex | ✅ | ✅ `codex` | Cursor, VS Code, Visual Studio, Antigravity, Kiro |
| Claude | ✅ | ✅ `claude` | Kiro, Cursor, VS Code, Visual Studio, Antigravity |
| Gemini | ✅ | ✅ `gemini` | VS Code, Cursor, Visual Studio, Antigravity, Kiro |
| Google AI Studio | ✅ | ❌ | VS Code (Gemini Code Assist), JetBrains, Cursor |
| Grok | ✅ | API only | VS Code, Cursor, Antigravity, Kiro |
| Groq | ✅ | via `curl` | VS Code, Cursor, Kiro |
| Kiro | ✅ | ✅ `kiro` | Kiro IDE, VS Code, Cursor, Visual Studio, Antigravity |
| MiniMax | ✅ | API only | VS Code, Cursor, Kiro |
| NotebookLM | ✅ | ❌ | None |
| Ollama | ✅ | ✅ `ollama` | VS Code (Continue), Cursor, Visual Studio, Kiro, Antigravity |
| OpenRouter | ✅ | via `curl` | VS Code, Cursor, Kiro, Antigravity |
| Kilo Code | ✅ | ✅ `kilo` | VS Code, JetBrains, Cursor |
| OpenCode | ✅ | ✅ `opencode` | VS Code (ACP), Cursor (ACP), JetBrains (ACP) |
| DeepSeek | ✅ | via `curl` | VS Code (Continue), Cursor, Kiro, JetBrains (Continue) |

See [TOOLS.md](TOOLS.md) for full details on each tool.

## Usage

1. Open `ai-control-center.html` in any browser (double-click the file)
2. Click **🌐 Open** to launch a tool's web interface
3. Click **Copy** next to any CLI command to copy it to your clipboard
4. Type in the **Notes** field for any tool — notes are saved automatically

No internet connection required to use the dashboard itself (only for launching the linked tools).

## Project Structure

```
ai-control-center/
├── ai-control-center.html   # The dashboard (single file, no dependencies)
├── README.md                # This file
├── TOOLS.md                 # Detailed documentation for each AI tool
└── CHANGELOG.md             # Version history
```

## Customization

The HTML file is self-contained and easy to edit:

- **Add a tool** — duplicate any `<div class="card">` block and update the content
- **Add a CLI command** — add a new `<div class="cli-block">` inside the tool's card
- **Add an IDE** — add a new `<span class="ide-badge">` inside the IDE list
- **Change theme colors** — edit the CSS variables at the top of the `<style>` block

## Notes Storage

Notes are saved in your browser's `localStorage` under keys `ai-notes-0` through `ai-notes-N`. They persist across browser sessions but are browser-specific. To back them up, copy the text manually.

## Requirements

- Any modern web browser (Chrome, Edge, Firefox, Safari)
- No server, no Node.js, no dependencies

## License

MIT
