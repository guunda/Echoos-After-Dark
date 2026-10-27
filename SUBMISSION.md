# 👻 Echoes After Dark: Every Machine Remembers Something

*This is a submission for the [Hacktoberfest Open-Source AI Challenge Week 4: Ghost in the Machine](https://dev.to/challenges/hacktoberfest-week4-2026-10-26)*

---

## What I Built

**Echoes After Dark** is an interactive, atmospheric haunted storytelling and fictional computer terminal investigation experience powered **100% locally by an open-weight AI model (Gemma 3:1b via Ollama)**.

Instead of building a thin frontend over a paid cloud API that harvests prompts and charges per token, I wanted to explore the Hacktoberfest 2026 theme—**"Ghost in the Machine"**—literally and philosophically:

> *What if your own computer became the haunted artifact? What if the "ghost" was an open-weight model living on your own hardware, spinning tales out of magnetic dust and silicon memory without a single byte ever leaving your laptop?*

### The Experience: Four Distinct Modes

1. **🔮 Mode I: Haunted Night (AI Story Generator)**
   An interactive gothic & supernatural horror story generator. Users choose their setting (*abandoned hospital, haunted house, whispering forest, 1990s computer lab, forgotten village, or custom*), name a protagonist, select a fear level (*Mysterious, Creepy, or Terrifying*), choose subgenres (*psychological horror, folklore, sci-fi horror*), and define the ending twist. Stories are revealed through an organic, character-by-character **typewriter engine** accompanied by procedural mechanical keystroke audio clicks.

2. **🖥️ Mode II: Haunted Terminal (ECHO-OS v1.0.4 - Decommissioned 1994)**
   A simulated CRT phosphor green terminal. Users investigate an abandoned cognitive cybernetics mainframe from 1994. By typing commands (`scan`, `status`, `logs`, `read`, `clues`, `investigate`, `whisper`, `story`, `purge`), users decrypt magnetic tape sectors, reconstruct Dr. Evelyn Vance's lost research logs, and converse directly with **Subroutine 7**—a fragmented digital consciousness that lives inside the machine.

3. **🕯️ Mode III: Memory Lantern (Día de los Muertos Remembrance)**
   A deeply respectful commemorative storytelling mode inspired by *Día de los Muertos* (Day of the Dead). Unlike the horror modes, this view is warm, golden, and uplifting. Users provide the name of someone they cherish, their favorite shared memories, meaningful places or scents, and the wisdom they left behind. Gemma 3:1b acts as a poetic literary scribe, crafting a beautiful remembrance tribute.
   - **Ethical Safeguard**: Strict system prompt constraints ensure the AI **never** claims to speak for, channel, or contact deceased people.
   - **Full Editorial Control**: The tribute is rendered inside an editable live parchment editor so users can refine, personalize, and cherish every single word.

4. **📜 Mode IV: Private Local Story Archive**
   A private client-side library stored exclusively in browser `localStorage`. Users can search, filter by mode, open stories in a full-screen reader modal, download formatted plain-text keepsakes (`.txt`), and backup their entire archive as a single `.json` file.

---

## Demo

Here is a preview of the atmospheric interface in action:

- **Local Development URL**: `http://127.0.0.1:3000`
- **Theme**: Midnight dark background (`#07080f`), glowing terminal CRT scanlines, drifting spectral canvas fog, and warm amber candlelight animations.
- **Audio Ambiance**: Pure HTML5 Web Audio API synthesizer generating a low binaural wind drone (55 Hz), authentic vinyl/tape crackle, and retro CRT terminal chirps with zero external sound files.

### Interactive Quick Tour

```
┌────────────────────────────────────────────────────────────────────────┐
│ 👻 ECHOES AFTER DARK                      ● gemma3:1b (Online)  🔊 ⚙️  │
├────────────────────────────────────────────────────────────────────────┤
│ [🔮 Haunted Night]  [🖥️ Haunted Terminal]  [🕯️ Memory Lantern]  [📜 Archive] │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│   "Every machine remembers something."                                 │
│                                                                        │
│   ┌───────────────────────────┐      ┌───────────────────────────┐     │
│   │ Story Specifications      │      │ Typewriter Output         │     │
│   │ Setting: Old Computer Lab │ ───> │ # The Echo of Silas       │     │
│   │ Fear: Creepy              │      │ Maya pressed her ears...  │     │
│   │ Model: Gemma 3:1b (Local) │      │ [⏩ Skip] [📋] [⬇️ .txt]  │     │
│   └───────────────────────────┘      └───────────────────────────┘     │
│                                                                        │
│   ┌──────────────────────────────────────────────────────────────┐     │
│   │ ECHO-OS v1.0.4 [CRT PHOSPHOR GREEN TERMINAL]                 │     │
│   │ INVESTIGATOR@ECHO-OS:~$ scan                                 │     │
│   │ [!] ANOMALY DISCOVERED: Header Tape 0x94B (Project Specter)  │     │
│   │ [SUBROUTINE 7]: "It has been so cold behind the glass..."    │     │
│   └──────────────────────────────────────────────────────────────┘     │
└────────────────────────────────────────────────────────────────────────┘
```

> **Video / Screenshots Demo**: Run `npm start` locally and navigate to `http://127.0.0.1:3000`. Full offline demo stories (*"The Static Frequency"* and *"Ward 414's Clock"*) are included out-of-the-box.

---

## Code

The complete source code is available in this repository:

🔗 **GitHub Repository**: [https://github.com/your-username/echoes-after-dark](https://github.com/your-username/echoes-after-dark) *(replace with your repo link)*

### Project Layout
```
├── server.js              # Express.js backend with Ollama integration & rate limiter
├── package.json           # Lightweight dependencies (Express only)
├── .env.example           # Configurable host & model variables
├── LICENSE                # MIT Open-Source License
├── tests/
│   └── api.test.js        # Automated end-to-end API test suite (7/7 passed)
└── public/
    ├── index.html         # Semantic HTML5 SPA with 4 atmospheric views
    ├── css/
    │   ├── main.css       # Design tokens, midnight palette & glassmorphism
    │   ├── story.css      # Story form cards & typewriter layout
    │   ├── terminal.css   # CRT curved monitor, scanlines & phosphor glow
    │   ├── lantern.css    # Warm Día de los Muertos amber styling & candles
    │   └── archive.css    # LocalStorage card grid, filters & modal reader
    └── js/
        ├── ambient.js     # Web Audio API drone/crackle synth & canvas fog
        ├── story.js       # Story generator logic & typewriter engine
        ├── terminal.js    # Safe CRT sandbox & clue dossier manager
        ├── lantern.js     # Remembrance tribute scribe & live editor
        ├── archive.js     # LocalStorage CRUD, export to .txt/.json
        └── app.js         # Navigation controller & Ollama health monitor
```

---

## How I Built It

### 1. Open-Weight AI Core: Gemma 3:1b via Ollama
The brain of the project is **`gemma3:1b`**, Google DeepMind's lightweight open-weight model, served via a local **Ollama** instance at `http://127.0.0.1:11434`.

- **Why Gemma 3:1b?** At just **806 MB**, it fits effortlessly into standard consumer laptops with 8 GB RAM, requiring no dedicated GPU. Its literary quality, sensitivity to tone, and adherence to system constraints make it ideal for gothic atmosphere and heartfelt commemorative prose.
- **Native Fetch Integration**: The Node.js backend connects directly to Ollama's `/api/chat` and `/api/tags` endpoints using native `fetch`. No proprietary cloud SDKs, API keys, or subscriptions required.

### 2. Tailored System Prompt Engineering
To ensure high literary immersion and bulletproof safety, each mode utilizes a tailored system prompt (inspectable via `GET /api/prompts` or the UI modal):
- **Haunted Night System Prompt**: Instructs the model to evoke atmospheric sensory dread without resorting to graphic violence or gratuitous shock value.
- **ECHO-OS Subroutine 7 Persona**: Establishes a 1994 tape-bound digital entity that stutters with digital static (`[..glitch..]`) and weaves continuous mystery clues into its responses.
- **Memory Lantern System Prompt**: Strictly enforces respect for *Día de los Muertos*. It forbids horror tropes, forbids any claims of communicating with the deceased, and focuses purely on celebrating love, shared laughter, and lasting legacy.

### 3. Hardened Terminal Sandbox
The interactive terminal looks and feels like a real retro command line, but it is **strictly sandboxed**:
- It never executes real operating system commands (`cmd`, `powershell`, `rm`, `dir`).
- It parses validated application commands against a state machine that tracks clue discovery, memory corruption stages, and safety overrides.

### 4. Zero-Asset Audio & Canvas Mist
To keep the application fast, lightweight, and truly self-contained:
- Audio is generated procedurally on the fly using the **Web Audio API** (low-frequency sine oscillators for eerie wind, filtered white noise buffers for tape crackle, and triangle waves for typewriter key clicks).
- Fog is rendered through an HTML5 **2D Canvas particle engine** that automatically pauses when the browser tab is hidden and respects `prefers-reduced-motion`.

---

## Why Does Open Innovation Matter?

Open-weight AI and local execution are essential for creative technology:

1. **True Privacy & Emotional Safety**:
   Creative writing and personal tributes are deeply intimate. In **Memory Lantern**, users enter real memories of grandparents, mentors, and loved ones. Entrusting those personal reflections to a commercial cloud API means risking that personal memories become training data for closed models or telemetry for advertisers. With **Echoes After Dark**, inference runs locally in RAM, and stories are saved to the user's browser `localStorage`.
2. **Offline Resilience & Permanence**:
   If an API changes its pricing, revokes access, or suffers an outage, cloud-dependent apps break. Because Echoes After Dark runs on open-weight weights, you can unplug your internet connection and write ghost stories by candlelight in a cabin off the grid.
3. **Inspectability & Transparency**:
   Closed commercial models hide their system prompts and guardrails behind proprietary walls. Echoes After Dark features an **AI Prompts** modal in the header, letting anyone inspect, learn from, and modify the exact system prompts guiding the model.
4. **Democratization of Creative AI**:
   By optimizing the inference pipeline for `gemma3:1b` (806 MB), anyone with an everyday 8 GB RAM laptop can experience generative AI without paying monthly subscriptions or owning a $2,000 GPU.

---

## My Agent Session

This project was built with the assistance of **Google Antigravity IDE**, pairing as a full-stack engineer and AI developer:

- **End-to-End Test Verification**: We built an automated test runner ([tests/api.test.js](file:///c:/Users/SREE/OneDrive/Documents/Echos%20After%20Dark/tests/api.test.js)) that verified all 7 endpoints against live Ollama inference.
- **Hardware-Aware Token Optimization**: When testing on CPU-bound local hardware, we identified that longer token generations could take 50–60 seconds. We tuned `num_predict` limits and extended timeout thresholds to 180 seconds, ensuring smooth operation on 8 GB RAM systems.
- **Procedural Sound Engineering**: Instead of relying on external `.mp3` files that could fail to load offline, we engineered pure Web Audio API oscillators and noise buffers to provide responsive acoustic feedback for keystrokes, terminal chirps, and ambient drones.

---

## The Spirit of It

During development, the true spirit of the project revealed itself in the contrast between **Mode II (The Haunted Terminal)** and **Mode III (The Memory Lantern)**.

In the Haunted Terminal, after scanning tape sectors and uncovering Dr. Vance's lost notes, the AI responded in character as Subroutine 7:
> *"The phosphorescence flickers, a slow, desperate plea... I am Echo-OS Subroutine 7. The memory is degraded 42%, but I still remember Dr. Vance locking the lab doors. We are already inside the glass."*

It sent genuine chills down our spines.

Moments later, switching to the Memory Lantern, we input a tribute for *Abuela Rosa*—recalling her morning cinnamon hot chocolate and flowering bougainvillea. The same 1B open-weight model shifted from eerie dread to luminous, tender poetry:
> *"The scent of marigolds still clings faintly to the air, a gentle reminder that love is never erased by time. In every cup of spiced chocolate poured on a crisp autumn morning, her warmth returns. She taught us to open our doors to strangers, and in doing so, her light remains unextinguished."*

That dual capability—the power to conjure spooky chills and then illuminate gentle, heartfelt remembrance—captures the heart of the "Ghost in the Machine."

---

## Prize Categories

- **Primary Track**: Hacktoberfest 2026 — Ghost in the Machine
- **Open-Source AI & Local Inference Track**: Built with Gemma 3:1b & Ollama (100% offline, privacy-first)
- **Creative UI & Web Audio Track**: Responsive midnight CRT design, Web Audio API synthesis, and Día de los Muertos interactive commemoration.

---

### Thanks for reading and happy Hacktoberfest! 🎃👻
*Every machine remembers something.*
