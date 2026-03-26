<p align="center">
  <img src="retrocode-icon.png" alt="RetroCode" width="200">
</p>

<h1 align="center">Senzall's RetroCode</h1>
<p align="center"><strong>Assembly & BASIC from 1980!</strong></p>
<p align="center">A free desktop IDE for learning 8-bit assembly language, BASIC programming, and modern code editing.<br>Three modes — Assembly, BASIC, and Code (ABC) — inspired by the Radio Shack Science Fair Microcomputer Trainer.</p>

---

## Download

| Platform | Download | Requirements |
|----------|----------|-------------|
| **macOS (Apple Silicon)** | [RetroCode_1.0.0_aarch64.dmg](https://github.com/senzalldev/retrocode-app/releases/latest/download/RetroCode_1.0.0_aarch64.dmg) | macOS 12+ (signed & notarized) |
| **macOS (Intel)** | [RetroCode-macOS-x64.zip](https://github.com/senzalldev/retrocode-app/releases/latest/download/RetroCode-macOS-x64.zip) | macOS 12+ |
| **Windows** | [RetroCode-Windows-x64.zip](https://github.com/senzalldev/retrocode-app/releases/latest/download/RetroCode-Windows-x64.zip) | Windows 10+ |
| **Linux** | [RetroCode-Linux-x64.zip](https://github.com/senzalldev/retrocode-app/releases/latest/download/RetroCode-Linux-x64.zip) | Ubuntu 22.04+ |

[All releases](https://github.com/senzalldev/retrocode-app/releases) | [Website](https://senzall.com/retrocode)
<!-- build-info --> _v1.0.0.3 · Build 20260326.1701_

> **Testing builds:** Want to try the latest features before they're stable?
> [Download the testing release](https://github.com/senzalldev/retrocode-app/releases/tag/v1.0.0-testing) (may have bugs)

---

## Screenshots

![Welcome](screenshots/welcome.png)

![Assembly Mode](screenshots/asm-mode.png)

![ASM Running](screenshots/asm-running.png)

![ASM Graphics](screenshots/asm-graphics.png)

![BASIC Terminal](screenshots/basic-terminal.png)

![BASIC Graphics](screenshots/basic-graphics.png)

![BASIC Lessons](screenshots/basic-lessons.png)

---

## What's Inside

### Assembly Mode
Write machine code for a simple 8-bit CPU with **36 instructions**. Watch registers change, memory update, and pixels appear on a 64x48 graphics display — all in real time.

- Step-through debugging — one instruction at a time
- Label support — modern assembler with forward references
- 19 example programs
- CPU state panel with registers, flags, and memory dump

### BASIC Mode
Program in BASIC V2.0, the language that came built into every home computer of the 1980s. A retro green terminal with a `>` prompt.

- 40+ commands — PRINT, INPUT, IF/THEN, FOR/NEXT, GOSUB, arrays, DATA/READ
- Math & string functions — SIN, COS, LEN, LEFT$, MID$, CHR$
- 64x48 bitmap graphics — PLOT, DRAW, CIRCLE, BOX, FILL
- Colon multi-statement support — `PRINT "A": PRINT "B"`
- 33 sample programs including Hangman and Reaction Timer

### Code Mode
A full-featured code editor with syntax highlighting for **23 programming languages**.

- **C, C++, C#, Java, JavaScript, TypeScript, Python, Ruby, Rust, Go, Swift, Kotlin, PHP, Perl, Lua, R, Shell/Bash, YAML, HTML, CSS, JSON, SQL, Markdown**
- Line numbers, find/replace, autocomplete, bracket matching, go-to-line, comment toggle, word wrap
- File browser with directory tree navigation
- Sample code for each language
- Auto-detects language from file extension

### Embedded Terminal
A built-in terminal (xterm.js) with shell selection, available as a global option in all three modes.

- Choose your shell (zsh, bash, etc.)
- Full terminal emulation
- Toggle from any mode

### Learn Tab
- **26 Assembly lessons** — from "What is a CPU?" to drawing graphics
- **25 BASIC lessons** — from "Hello World" to building complete programs
- Built-in reference panels always visible

---

## Quick Reference

### Assembly (36 opcodes)

```
LDI 0A      ; Load 10 into A
LBI 05      ; Load 5 into B
ADD         ; A = A + B = 15
OUT         ; Display A
LOOP: DEC   ; A = A - 1 (label!)
JNZ LOOP    ; Jump back if not zero
PLT         ; Plot pixel at (A, B)
HLT         ; Stop
```

### BASIC

```basic
10 PRINT "HELLO WORLD"
20 FOR I = 1 TO 10
30 PRINT I * I
40 NEXT I
50 CIRCLE 32, 24, 15
60 END
```

---

## Features

- **3 modes** — Assembly, BASIC, and Code (ABC)
- **23 programming languages** with syntax highlighting
- **Split-pane IDE** with code editor + CPU state / terminal / graphics
- **Embedded terminal** (xterm.js) with shell selection — global option in all modes
- **File browser** — directory tree navigation
- **6 themes** — Default (green), Standard, Dark, Light, RPG, High Contrast
- **Editor features** — line numbers, find/replace, autocomplete, bracket matching, go-to-line, comment toggle, word wrap
- **MCP API** for Claude integration (port 21580)
- **Settings** — theme picker, CPU speed slider, zoom
- **File I/O** — save/load .asm, .bas, .hex files
- **UI zoom** — 75% to 150%
- **Keyboard shortcuts** — Cmd+R, Cmd+S, F10
- **210 unit tests**

---

## Claude Integration (MCP)

RetroCode includes a built-in MCP (Model Context Protocol) server that lets Claude interact with the IDE directly.

**Setup (2 steps):**
1. In RetroCode: **Code → MCP tab → "Save mcp-server.js to Home Folder"**
2. In your terminal: `claude mcp add retrocode node ~/mcp-server.js`

**8 MCP tools:**
- `retrocode_get_editor` — read content, mode, language, file path
- `retrocode_set_editor` — write code with language (auto-switches highlighting)
- `retrocode_append_editor` — add code to editor
- `retrocode_read_file` — read a file from disk
- `retrocode_save_file` — save editor to disk
- `retrocode_list_languages` — list all 23 supported languages
- `retrocode_get_mode` — check current mode
- `retrocode_health` — verify connection

**API endpoints** (port 21580):
- `GET /api/health` — check status
- `GET /api/editor` — read editor state
- `PUT /api/editor` — write to editor (with language)
- `POST /api/editor/append` — append to editor
- `GET /api/readfile?path=...` — read file from disk
- `POST /api/savefile` — save content to file

The MCP server runs on **port 21580** whenever RetroCode is open.

---

## Documentation

| Topic | Link |
|-------|------|
| Getting Started | [Wiki: Getting Started](https://github.com/senzalldev/retrocode-app/wiki/Getting-Started) |
| Assembly Reference (36 opcodes) | [Wiki: Assembly Reference](https://github.com/senzalldev/retrocode-app/wiki/Assembly-Reference) |
| BASIC Reference (40+ commands) | [Wiki: BASIC Reference](https://github.com/senzalldev/retrocode-app/wiki/BASIC-Reference) |
| Code Editor (23 languages) | [Wiki: Code Editor](https://github.com/senzalldev/retrocode-app/wiki/Code-Editor) |
| MCP Integration (Claude AI) | [Wiki: MCP Integration](https://github.com/senzalldev/retrocode-app/wiki/MCP-Integration) |
| Graphics Guide (64x48 bitmap) | [Wiki: Graphics Guide](https://github.com/senzalldev/retrocode-app/wiki/Graphics-Guide) |
| Assembly Lessons (26) | [Wiki: Assembly Lessons](https://github.com/senzalldev/retrocode-app/wiki/Assembly-Lessons) |
| BASIC Lessons (25) | [Wiki: BASIC Lessons](https://github.com/senzalldev/retrocode-app/wiki/BASIC-Lessons) |
| Keyboard Shortcuts | [Wiki: Keyboard Shortcuts](https://github.com/senzalldev/retrocode-app/wiki/Keyboard-Shortcuts) |
| FAQ | [Wiki: FAQ](https://github.com/senzalldev/retrocode-app/wiki/FAQ) |

---

## The Story

In 7th grade, Senzall's dad surprised him with a TRS-80 Color Computer — powered by the Motorola 6809 CPU that his dad's team at Motorola helped build. Before that, he'd been writing BASIC programs at Radio Shack store windows since age 12. RetroCode recreates that experience for a new generation.

---

**[senzall.com/retrocode](https://senzall.com/retrocode)** | **[Download](https://github.com/senzalldev/retrocode-app/releases/latest)** | **[Report Issue](https://github.com/senzalldev/retrocode-app/issues)**

Copyright 2026 Senzall. All rights reserved. Free to download and use.
