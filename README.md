# Senzall's RetroCode

**Assembly & BASIC from 1980!**

A standalone desktop IDE for learning 8-bit assembly language and BASIC programming, inspired by the Radio Shack Science Fair Microcomputer Trainer and the home computers of the 1980s.

![RetroCode Screenshot](https://senzall.com/retrocode/screenshot.png)

---

## Download

| Platform | Download | Requirements |
|----------|----------|-------------|
| **macOS (Apple Silicon)** | [RetroCode-macOS-arm64.zip](https://github.com/senzalldev/retrocode/releases/latest/download/RetroCode-macOS-arm64.zip) | macOS 12+ (M1/M2/M3) |
| **macOS (Apple Silicon DMG)** | [RetroCode_1.0.0_aarch64.dmg](https://github.com/senzalldev/retrocode/releases/latest/download/Senzalls.RetroCode_1.0.0_aarch64.dmg) | macOS 12+ (signed & notarized) |
| **macOS (Intel)** | [RetroCode-macOS-x64.zip](https://github.com/senzalldev/retrocode/releases/latest/download/RetroCode-macOS-x64.zip) | macOS 12+ (Intel) |
| **Windows** | [RetroCode-Windows-x64.zip](https://github.com/senzalldev/retrocode/releases/latest/download/RetroCode-Windows-x64.zip) | Windows 10+ |

[All releases](https://github.com/senzalldev/retrocode/releases)

---

## What is RetroCode?

RetroCode is a learning tool that recreates the experience of programming on early home computers. It has two modes:

### Assembly Mode
Write machine code for a simple 8-bit CPU with 36 instructions. Watch registers change, memory update, and pixels appear on a 64x48 graphics display — all in real time.

- **36 opcodes** — data movement, arithmetic, logic, branching, stack, graphics
- **Label support** — modern assembler with forward references
- **Step-through debugging** — execute one instruction at a time
- **CPU state panel** — registers, flags, output, memory dump
- **19 example programs** — from "Hello Display" to animated graphics

### BASIC Mode
Program in BASIC V2.0, the language that came built into nearly every home computer of the 1980s. A retro green terminal with a `>` prompt, just like the old days.

- **40+ commands** — PRINT, INPUT, IF/THEN, FOR/NEXT, GOSUB, arrays, DATA/READ
- **Math & string functions** — SIN, COS, TAN, LEN, LEFT$, MID$, CHR$, and more
- **64x48 bitmap graphics** — PLOT, DRAW, CIRCLE, BOX, FILL
- **Virtual file system** — SAVE$, LOAD$, DIR for persistent storage
- **31 sample programs** — games, math plots, utilities, graphics demos

### Learning System
Both modes include a **Learn** tab with progressive lessons:

- **26 Assembly lessons** — from "What is a CPU?" to drawing graphics
- **25 BASIC lessons** — from "Welcome to BASIC" to building complete programs
- **Built-in reference panels** — quick reference + detailed documentation always visible

---

## Features

- **Split-pane IDE** — code editor on the left, CPU state / terminal / graphics on the right
- **4 themes** — Retro (green terminal), Dark, Light (Apple-standard), RPG
- **Graphics display** — 64x48 pixel bitmap with PLOT, DRAW, CIRCLE, BOX, FILL
- **File I/O** — save and load .asm, .bas, .hex files
- **UI zoom** — 75% to 150% for any screen size
- **Keyboard shortcuts** — Cmd+R (run), Cmd+S (save), F10 (step)
- **133 unit tests** — comprehensive test coverage

---

## Screenshots

### Assembly Mode
![Assembly Mode](https://senzall.com/retrocode/asm-mode.png)

### BASIC Terminal
![BASIC Terminal](https://senzall.com/retrocode/basic-terminal.png)

### Graphics Display
![Graphics](https://senzall.com/retrocode/graphics.png)

### Learn Tab
![Lessons](https://senzall.com/retrocode/lessons.png)

---

## Documentation

Full documentation is available at **[senzall.com/retrocode](https://senzall.com/retrocode)** and in the [Wiki](https://github.com/senzalldev/retrocode-app/wiki).

### Quick Start
1. Download and install RetroCode for your platform
2. Choose **Assembly** or **BASIC** mode
3. Click the **Learn** tab in the right panel to start lessons
4. Or click **Examples/Samples** to load a program and hit **Run**

### Assembly Quick Reference

| Instruction | Description |
|------------|-------------|
| `LDI 0A` | Load value 0A into register A |
| `LBI 05` | Load value 05 into register B |
| `ADD` | A = A + B |
| `SUB` | A = A - B |
| `OUT` | Display register A |
| `CPI 0A` | Compare A with 0A |
| `JZ LABEL` | Jump to LABEL if zero flag set |
| `JNZ LOOP` | Jump to LOOP if not zero |
| `PLT` | Plot pixel at (A, B) |
| `HLT` | Stop execution |

Labels: `LOOP: INC` defines a label. Use as jump target: `JNZ LOOP`

### BASIC Quick Reference

```basic
10 PRINT "HELLO WORLD"
20 LET A = 5
30 INPUT "NAME"; N$
40 IF A > 3 THEN GOTO 70
50 FOR I = 1 TO 10
60 NEXT I
70 GOSUB 200
80 PLOT 32, 24
90 END
200 PRINT "SUBROUTINE"
210 RETURN
```

---

## The Story Behind RetroCode

In 7th grade, Senzall's dad surprised him with a TRS-80 Color Computer — powered by the Motorola 6809 CPU that his dad's team at Motorola helped build. Before that, he'd been writing BASIC programs at Radio Shack store windows since age 12. By 1983 he had an IBM PC, learning 8088 assembly and Turbo Pascal.

RetroCode recreates that experience — inspired by the Radio Shack Science Fair Microcomputer Trainer and the home computers of the 1980s. It's built for anyone who wants to understand how computers really work, one instruction at a time.

---

## System Requirements

- **macOS**: 12.0 or later (Apple Silicon or Intel)
- **Windows**: 10 or later (64-bit, WebView2 included)

---

## License

Copyright 2026 Senzall. All rights reserved.

RetroCode is free to download and use. Source code is proprietary.

---

**Made with love by [Senzall](https://senzall.com)** | [Website](https://senzall.com/retrocode) | [Report an Issue](https://github.com/senzalldev/retrocode-app/issues)
