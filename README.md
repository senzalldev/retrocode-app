<p align="center">
  <img src="retrocode-icon.png" alt="RetroCode" width="200">
</p>

<h1 align="center">Senzall's RetroCode</h1>
<p align="center"><strong>1980s Computing Meets Modern AI</strong></p>
<p align="center">Write 8-bit assembly. Program in BASIC. Code in 25 languages. Chat with Claude or GitHub Copilot.<br>Three modes — Assembly, BASIC, and Code — inspired by the TRS-80, Apple II, and Commodore 64.</p>

---

## Download

| Platform | Download | Requirements |
|----------|----------|-------------|
| **macOS (Apple Silicon)** | [RetroCode-macOS-arm64.dmg](https://github.com/senzalldev/retrocode-app/releases/latest/download/RetroCode-macOS-arm64.dmg) | macOS 12+ (signed & notarized) |
| **Windows** | [RetroCode-Windows-x64.zip](https://github.com/senzalldev/retrocode-app/releases/latest/download/RetroCode-Windows-x64.zip) | Windows 11+ |

[All releases](https://github.com/senzalldev/retrocode-app/releases) | [Website](https://senzall.com/retrocode)
<!-- build-info --> _v1.3.0.2 · Build 20260402.0116_

---

## AI Integration (Claude + GitHub Copilot)

Chat with AI directly inside RetroCode. Your AI assistant can write code, save files, run scripts, and manage tabs — all through the chat panel. Choose your provider in **Settings > AI Provider**.

### Option A: Claude (via MCP)

Uses your Claude Max/Pro subscription through Claude Code CLI.

1. **In RetroCode:** Code → MCP tab → click **"Install MCP + /retrocode Command"**
2. **In your terminal:** `claude mcp add retrocode node ~/mcp-server.js`
3. **Start a session:** Type `/retrocode` in Claude Code
4. **Tip:** Type `/fast` first for faster responses

### Option B: GitHub Copilot (via SDK)

Uses your GitHub Copilot subscription. Access GPT-4.1, Claude, Gemini, and more — pick the model in Settings.

1. **Install:** `npm install -g @github/copilot @github/copilot-sdk`
2. **Authenticate:** `copilot auth login`
3. **Start:** `node ~/copilot-bridge.js` (or `node ~/copilot-bridge.js --model claude-sonnet-4`)
4. **List models:** `node ~/copilot-bridge.js --list-models`

### How It Works

**Claude** uses MCP (Model Context Protocol) — a JSON-RPC bridge that gives Claude 23 tools to control RetroCode. The poll script detects your messages and forwards them.

**Copilot** uses the GitHub Copilot SDK — a bridge script polls the chat API, sends messages to the Copilot backend (with your chosen model), and posts responses back. Same 13 core tools (editor, files, terminal, references).

Both providers keep token usage low — they only activate when you send a message.

### Available Models (Copilot)

| Model | Tier |
|-------|------|
| GPT-4.1, GPT-4o, GPT-4.1 Mini | Included |
| Claude Sonnet 4/4.5, Gemini 3 Pro, o3-mini | 1x premium |
| Claude Haiku 4.5, Gemini 3 Flash | 0.33x premium |
| Claude Opus 4.5/4.6 | 3x premium |

### 23 MCP Tools (Claude)
| Category | Tools |
|----------|-------|
| Editor | get, set, append |
| Files | save, read |
| Tabs | list, switch, new |
| Terminal | open, close, command, output |
| Chat | send, read, heartbeat |
| Control | run, stop, switch mode, get mode |
| Reference | ASM reference, BASIC reference |
| System | health, languages |

---

## Screenshots

![Welcome](screenshots/welcome.png)

![Assembly Mode](screenshots/asm-mode.png)

![BASIC Terminal](screenshots/basic-terminal.png)

---

## Features

- **3 modes** — Assembly, BASIC, and Code (ABC)
- **8-Bit CPU Simulator** — 36 instructions, step-through debugging, labels
- **BASIC V2.0** — 40+ commands, graphics, DATA/READ, PEEK/POKE, virtual file system
- **INKEY$ game support** — Arrow keys, WASD, SPACE detection for real-time games (Snake, Breakout)
- **64x48 Graphics Display** — PLOT, DRAW, CIRCLE, BOX, FILL
- **Code Editor** — 25 languages with syntax highlighting
- **Per-mode file tabs** — up to 5 tabs in each mode with session recovery
- **Multiple terminals** — up to 4 concurrent sessions with tab switching
- **Collapsible sidebar** — toggle the right panel in any mode
- **51 lessons** — 26 assembly + 25 BASIC
- **50+ sample programs** — Snake, Breakout, math plots, trig functions
- **AI chat** — Claude (via MCP) or GitHub Copilot (via SDK) with 11 model choices
- **6 themes** — Default, Standard, Dark, Light, RPG, High Contrast
- **File browser** — directory tree navigation
- **Embedded terminal** (xterm.js) — global option in all modes

---

## Documentation

- [Website](https://senzall.com/retrocode)
- [Wiki](https://github.com/senzalldev/retrocode-app/wiki)
- [Report an Issue](https://github.com/senzalldev/retrocode-app/issues)

---

Copyright 2026 [Senzall](https://senzall.com). All rights reserved.
