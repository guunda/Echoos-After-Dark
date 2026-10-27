# 👻 Echoes After Dark

> *"Every machine remembers something."*

An interactive haunted storytelling and fictional computer terminal investigation experience powered **100% locally by open-weight AI (Gemma 3:1b via Ollama)**.

Created for the **Hacktoberfest 2026 "Ghost in the Machine" Open-Source AI Challenge**.

[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg)](LICENSE)
[![GitHub Repository](https://img.shields.io/badge/GitHub-guunda%2FEchoos--After--Dark-181717.svg?logo=github)](https://github.com/guunda/Echoos-After-Dark)
[![AI Model](https://img.shields.io/badge/AI_Model-Gemma_3:1b-purple.svg)](https://ollama.com/library/gemma3)
[![Local Inference](https://img.shields.io/badge/Inference-100%25_Local_(Ollama)-blue.svg)](https://ollama.ai)
[![Node.js](https://img.shields.io/badge/Node.js-v18%2B-green.svg)](https://nodejs.org)
[![Privacy](https://img.shields.io/badge/Privacy-100%25_Local_Storage-success.svg)](#privacy--safeguards)

---

## 📖 Table of Contents
1. [Project Overview](#-project-overview)
2. [Why Open-Weight AI & Local Innovation Matter](#-why-open-weight-ai--local-innovation-matter)
3. [Key Features](#-key-features)
   - [Mode I: Haunted Night (AI Story Generator)](#mode-i-haunted-night-ai-story-generator)
   - [Mode II: Haunted Terminal (ECHO-OS 1994)](#mode-ii-haunted-terminal-echo-os-1994)
   - [Mode III: Memory Lantern (Día de los Muertos Remembrance)](#mode-iii-memory-lantern-d%C3%ADa-de-los-muertos-remembrance)
   - [Mode IV: Private Local Story Archive](#mode-iv-private-local-story-archive)
4. [Architecture & Technology Stack](#%EF%B8%8F-architecture--technology-stack)
5. [System Requirements](#-system-requirements)
6. [Quick Start & Installation](#-quick-start--installation)
   - [Step 1: Install Ollama & Download Gemma 3:1b](#step-1-install-ollama--download-gemma-31b)
   - [Step 2: Install App Dependencies & Launch](#step-2-install-app-dependencies--launch)
7. [API Endpoint Documentation](#-api-endpoint-documentation)
8. [Privacy, Security & Safeguards](#-privacy-security--safeguards)
9. [Automated Testing Suite](#-automated-testing-suite)
10. [Known Hardware Characteristics & Limitations](#-known-hardware-characteristics--limitations)
11. [Contributing to Hacktoberfest 2026](#-contributing-to-hacktoberfest-2026)
12. [License](#-license)

---

## 🌟 Project Overview

**Echoes After Dark** is a browser-based supernatural creative writing suite that transforms your computer into a haunted machine. Rather than relying on cloud subscriptions or remote APIs that harvest your prompts, Echoes After Dark runs entirely on your own laptop using **Gemma 3:1b**—Google DeepMind's state-of-the-art open-weight lightweight language model.

Users can:
1. Summon original supernatural, psychological, or sci-fi horror tales with customizable parameters and typewriter pacing.
2. Step inside **ECHO-OS**, a simulated 1994 decommissioned laboratory mainframe, to decrypt magnetic tape sectors and converse with a digital ghost subroutine.
3. Light a **Memory Lantern**, a respectful, warm commemorative storytelling mode inspired by *Día de los Muertos* to celebrate cherished memories of loved ones.
4. Curate a private library stored exclusively in browser `localStorage`, with instant plain-text (`.txt`) and `.json` backup exports.

---

## 💡 Why Open-Weight AI & Local Innovation Matter

Most commercial AI storytelling platforms lock users into expensive cloud subscriptions, send creative writings to external servers for telemetry and advertising, and restrict how users can customize prompts.

**Echoes After Dark** takes a fundamentally different stance:
- **Zero Cloud Dependence**: The model runs locally via Ollama on `localhost:11434`. After the initial model download, you can disconnect your Wi-Fi and generate stories offline in a secluded cabin in the woods.
- **Uncompromised Privacy**: Your stories, character names, and personal family memories never leave your machine.
- **Inspectable & Hackable**: All system prompts are accessible in the UI (`/api/prompts`) and can be modified directly in `server.js`.
- **Model Agnostic**: Easily swap `gemma3:1b` with `gemma4:latest`, `qwen2.5-coder:3b`, `mistral`, or `llama3.2:1b` by changing a single environment variable (`OLLAMA_MODEL`).

---

## 🔮 Key Features

### Mode I: Haunted Night (AI Story Generator)
- **Granular Atmospheric Controls**:
  - **Settings**: Abandoned Hospital, Haunted House, Whispering Forest, Old Computer Lab, Forgotten Village, or custom setting input.
  - **Protagonist**: Name and background of who enters the unknown.
  - **Length**: Short (~200 words), Medium (~400 words), or Long (~700 words).
  - **Fear Level**: *Mysterious* (subtle, eerie psychological), *Creepy* (uncanny, rising dread), or *Terrifying* (high tension, intense climax).
  - **Subgenres**: Supernatural Mystery, Psychological Horror, Folklore-Inspired Fiction, Sci-Fi Horror.
  - **Ending**: Unexpected Twist, Unresolved Mystery, or Hopeful Escape.
- **Dynamic Typewriter Engine**: Organic character-by-character reveal with mechanical sound effects and instant skip control.
- **Quick Action Bar**: Copy to clipboard, export as `.txt`, save to local archive, or regenerate.
- **Offline Demonstration Mode**: Pre-loaded example stories allow users to test the reading experience even if Ollama is temporarily stopped.

### Mode II: Haunted Terminal (ECHO-OS 1994)
- **Authentic Vintage CRT Simulation**: Curved screen borders, phosphor green glow, CRT scanlines, and audio feedback.
- **Safe Command Sandbox**:
  - `scan`: Scans corrupted magnetic tape sectors to uncover hidden artifacts.
  - `status`: Displays simulated Motorola 68040 CPU readings, corrupted parity RAM, and infrasound frequency.
  - `logs`: Decrypts 1994 laboratory logs detailing Dr. Evelyn Vance's cognitive cybernetics experiments.
  - `read <log_id>`: Reads decrypted log files.
  - `clues`: Lists gathered evidence artifacts.
  - `investigate <id>`: Instructs Subroutine 7 to generate a localized anomaly description.
  - `whisper <query>`: Directly questions the trapped 1994 digital consciousness using Ollama.
  - `story`: Synthesizes an interactive mystery climax weaving together all discovered clues.
  - `purge`: Attempts emergency security deionization.
  - `clear` & `exit`: Utility controls.
- **Strict Execution Safety**: Safe emulation only. The terminal **never** executes real operating system commands, inspects host files, or spawns shell processes.

### Mode III: Memory Lantern (Día de los Muertos Remembrance)
- **Respectful Commemoration**: Inspired by the tradition of *Día de los Muertos* (Day of the Dead), this mode celebrates life and honors legacy.
- **Cultural Safeguard Guidelines**:
  - Never claims to channel, contact, or speak on behalf of deceased people.
  - Completely separated from horror aesthetics: warm cempasúchil marigold orange, golden candlelight flames, and terracotta tones.
- **Interactive Live Scribe**: Enter cherished memories, meaningful places, favorite scents, and enduring wisdom. Gemma 3:1b weaves a gentle, poetic tribute.
- **Full Editorial Control**: The generated tribute is rendered inside an editable parchment editor, allowing you to personalize every line before saving.

### Mode IV: Private Local Story Archive
- **Client-Side Persistence**: Saved entries are written to browser `localStorage`.
- **Search & Filter**: Real-time search across titles, characters, and text, with one-click filters for Haunted Night vs. Memory Lantern entries.
- **Reader Modal**: Full-screen distraction-free reader with metadata inspection.
- **Export Capabilities**:
  - Single story download as `.txt` formatted keepsake.
  - Complete archive backup export as JSON (`.json`).
  - Safe archive purge with confirmation dialog.

---

## 🛠️ Architecture & Technology Stack

```
Echos After Dark/
├── server.js               # Node.js & Express server with Ollama integration
├── package.json            # Minimal dependencies (Express only)
├── .env.example            # Configurable environment variables
├── README.md               # Hacktoberfest 2026 documentation
├── LICENSE                 # MIT Open-Source License
├── tests/
│   └── api.test.js         # Automated end-to-end API test suite
└── public/
    ├── index.html          # Semantic HTML5 SPA layout
    ├── css/
    │   ├── main.css        # Midnight design system, variables, modals, fog
    │   ├── story.css       # Story generator controls & typewriter display
    │   ├── terminal.css    # Retro CRT monitor, phosphor green glow & dossier
    │   ├── lantern.css     # Día de los Muertos warm theme & candle animations
    │   └── archive.css     # LocalStorage card grid, search bar & filters
    └── js/
        ├── ambient.js      # Web Audio API synthesizer & canvas mist particles
        ├── archive.js      # LocalStorage CRUD, export & reader modal
        ├── story.js        # Generator form logic, typewriter engine & samples
        ├── terminal.js     # Safe CRT emulator, clue tracker & command history
        ├── lantern.js      # Remembrance tribute generator & live editor
        └── app.js          # Navigation controller & Ollama health monitor
```

### Technology Highlights:
- **Backend**: Node.js v18+ & Express.js. Native `fetch` with zero heavy SDKs.
- **Local AI Provider**: Ollama REST API (`/api/chat` and `/api/tags`).
- **Default AI Model**: `gemma3:1b` (806 MB, Google DeepMind).
- **Frontend**: Vanilla HTML5, Vanilla CSS3 (Custom Properties, Flexbox/Grid, Glassmorphism), Vanilla JavaScript (ES2022). No bloated frameworks.
- **Audio Synthesis**: Pure HTML5 Web Audio API (real-time generated binaural drone, tape crackle, CRT chirps, and typewriter clicks—no external sound files required).
- **Atmosphere**: Canvas 2D spectral mist particle engine with `prefers-reduced-motion` compliance.

---

## 💻 System Requirements

Designed specifically to run smoothly on everyday consumer laptops:
- **Operating System**: Windows 10/11, macOS, or Linux.
- **RAM**: 8 GB RAM minimum (Gemma 3:1b requires only ~1.2 GB of available memory).
- **Disk Space**: ~1 GB free space for the model weights and dependencies.
- **Node.js**: v18.0.0 or higher (Node v20+ recommended).
- **Ollama**: v0.1.30 or higher.

---

## 🚀 Quick Start & Installation

### Step 1: Install Ollama & Download Gemma 3:1b

1. Download and install **Ollama** from [https://ollama.com/download](https://ollama.com/download).
2. Open your terminal (PowerShell or Bash) and pull the model:
   ```bash
   ollama pull gemma3:1b
   ```
3. Verify that the model is ready:
   ```bash
   ollama list
   ```
   You should see `gemma3:1b` listed with a size of ~806 MB.

4. Ensure Ollama is running:
   ```bash
   ollama serve
   ```
   *(On Windows, Ollama usually runs automatically in the system tray).*

### Step 2: Install App Dependencies & Launch

1. Clone the repository and navigate into the folder:
   ```bash
   git clone https://github.com/guunda/Echoos-After-Dark.git
   cd Echoos-After-Dark
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the application:
   ```bash
   npm start
   ```

4. Open your browser and navigate to:
   ```
   http://127.0.0.1:3000
   ```

The AI status badge in the top right will display a glowing green dot: `gemma3:1b (Online)`.

---

## 📡 API Endpoint Documentation

| Method | Endpoint | Description | Sample Request / Response |
| :--- | :--- | :--- | :--- |
| `GET` | `/api/health` | Pings Ollama and verifies model availability. | `{ "status": "ok", "ollamaConnected": true, "configuredModel": "gemma3:1b", "modelAvailable": true }` |
| `GET` | `/api/prompts` | Open-weight transparency endpoint returning current system instructions. | `{ "model": "gemma3:1b", "prompts": { "hauntedStory": "...", ... } }` |
| `POST` | `/api/generate-story` | Generates an original ghost story using Gemma 3. | Body: `{ "setting": "old computer lab", "character": "Maya", "length": "short", "fearLevel": "creepy", "storyType": "science-fiction horror", "ending": "unexpected twist" }` |
| `POST` | `/api/terminal` | Processes simulated ECHO-OS terminal commands and Subroutine 7 dialogue. | Body: `{ "command": "scan", "currentClues": [], "stage": 0 }` |
| `POST` | `/api/memory-lantern` | Crafts a commemorative Día de los Muertos remembrance tribute. | Body: `{ "name": "Abuela Rosa", "memories": "warm chocolate and laughter", "places": "autumn patio", "lessons": "kindness" }` |

---

## 🔒 Privacy, Security & Safeguards

- **Bound to Localhost**: The server defaults to `127.0.0.1` to prevent unauthorized external network access.
- **Zero Real Command Execution**: The haunted terminal strictly rejects operating system commands (`dir`, `del`, `rm`, `cat`, etc.) and runs a hardened virtual state machine.
- **In-Memory Concurrency Limiter**: Automatically manages request concurrency to avoid exhausting memory on 8 GB RAM laptops.
- **Local Persistence Only**: Stories, notes, and tributes are stored strictly inside your browser's private `localStorage`.
- **Injection Defenses**: Creative inputs are sanitized, length-limited, and framed strictly as creative storytelling variables to prevent prompt manipulation.

---

## 🧪 Automated Testing Suite

Echoes After Dark includes a built-in automated test suite verifying every endpoint against real Ollama inference:

Run tests with:
```bash
npm test
```

Expected output:
```text
🧪 Starting Echoes After Dark API Test Suite at http://127.0.0.1:3000...
  • Testing GET /api/health... (Ollama: Connected, Model: gemma3:1b, Available: true) ✅ PASSED
  • Testing GET /api/prompts... ✅ PASSED
  • Testing POST /api/terminal (help command)... ✅ PASSED
  • Testing POST /api/terminal (scan command adds clue)... ✅ PASSED
  • Testing POST /api/terminal (AI whisper command)... ✅ PASSED
  • Testing POST /api/generate-story (gemma3:1b)... ✅ PASSED
  • Testing POST /api/memory-lantern (remembrance tribute)... ✅ PASSED

=============================================
Results: 7 passed, 0 failed.
=============================================
```

---

## ⚠️ Known Hardware Characteristics & Limitations

- **CPU vs GPU Inference**: When running Ollama on standard laptop CPUs without a dedicated GPU, generating a 200-word story typically takes 30–50 seconds. This is normal for local on-device inference.
- **Browser LocalStorage**: LocalStorage is isolated to your specific browser profile. If you clear browser website data or switch browsers, export your stories using the `Export All (.json)` button first.

---

## 🤝 Contributing to Hacktoberfest 2026

We welcome contributions from open-source developers, writers, and AI enthusiasts!
1. Fork the repository at [https://github.com/guunda/Echoos-After-Dark](https://github.com/guunda/Echoos-After-Dark).
2. Create your feature branch (`git checkout -b feature/spectral-audio`).
3. Commit your changes (`git commit -m 'Add new CRT phosphor color modes'`).
4. Push to the branch (`git push origin feature/spectral-audio`).
5. Open a Pull Request tagged with `hacktoberfest`.

---

## 📄 License

This project is open-source under the terms of the **[MIT License](LICENSE)**.
Model weights for **Gemma 3** are subject to the [Gemma Terms of Use](https://ai.google.dev/gemma/terms).
