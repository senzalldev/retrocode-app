<p align="center">
  <img src="retrocode-icon.png" alt="RetroCode" width="200">
</p>

<h1 align="center">Senzall's RetroCode</h1>
<p align="center"><strong>1980s Computing Meets Modern AI</strong></p>
<p align="center">Write 8-bit assembly. Program in BASIC. Code in 25 languages. And let Claude AI help you along the way.<br>Three modes — Assembly, BASIC, and Code — inspired by the TRS-80, Apple II, and Commodore 64.</p>

---

## Download

| Platform | Download | Requirements |
|----------|----------|-------------|
| **macOS (Apple Silicon)** | [RetroCode-macOS-arm64.dmg](https://github.com/senzalldev/retrocode-app/releases/latest/download/RetroCode-macOS-arm64.dmg) | macOS 12+ (signed & notarized) |
| **Windows** | [RetroCode-Windows-x64.zip](https://github.com/senzalldev/retrocode-app/releases/latest/download/RetroCode-Windows-x64.zip) | Windows 11+ |

[All releases](https://github.com/senzalldev/retrocode-app/releases) | [Website](https://senzall.com/retrocode)
<!-- build-info --> _v1.2.0.5 · Build 20260331.0121_

---

## Claude AI Integration

Chat with Claude directly inside RetroCode. Claude can write code, save files, run scripts, and manage tabs — all through the chat panel.

### Setup (one time)
1. **In RetroCode:** Code → MCP tab → click **"Install MCP + /retrocode Command"** (saves 3 files, copies command to clipboard)
2. **In your terminal:** Paste the command (already copied): `claude mcp add retrocode node ~/mcp-server.js`
3. **Start a session:** Type `/retrocode` in Claude Code (or `/retrocode 3` for faster polling)
4. **Tip:** Type `/fast` first for faster responses and lower token usage

### How It Works

The install button saves three files:
- **~/mcp-server.js** — 23 MCP tools Claude uses to control RetroCode
- **~/retrocode-poll.js** — Chat proxy that bridges messages to Claude
- **~/.claude/commands/retrocode.md** — The /retrocode slash command

When you type in the RetroCode chat panel, the proxy script detects your message and passes it to Claude. Claude responds via MCP tools. Heartbeats and connection status are handled automatically — Claude is only invoked when you send a message, keeping token usage low.

### 23 MCP Tools
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
- **64x48 Graphics Display** — PLOT, DRAW, CIRCLE, BOX, FILL
- **Code Editor** — 25 languages with syntax highlighting
- **Per-mode file tabs** — up to 5 tabs in each mode with session recovery
- **Multiple terminals** — up to 4 concurrent sessions with tab switching
- **Collapsible sidebar** — toggle the right panel in any mode
- **51 lessons** — 26 assembly + 25 BASIC
- **50+ sample programs** — games, math plots, trig functions
- **23 MCP tools** for Claude AI integration
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
