# ACE-Step Studio

A single-file HTML/JS interface for [ACE-Step 1.5](https://github.com/ace-step/ACE-Step-1.5) — the open-source music generation model. No installation required beyond ACE-Step itself.

![ACE-Step Studio](https://img.shields.io/badge/ACE--Step-1.5-blue) ![HTML](https://img.shields.io/badge/HTML-single--file-green)

---
<img width="2557" height="1235" alt="Capture d&#39;écran 2026-04-16 072216" src="https://github.com/user-attachments/assets/24a1f484-7adb-44e8-be18-f9f66f6cbb82" />

## Features

- **Compose** — Text-to-music generation with full parameter control
- **Cover** — Style transfer from a reference audio
- **Repaint** — Selective region editing with WaveSurfer timeline
- **Base ★** — Exclusive Base model modes:
  - 🧱 **Lego** — Add a specific instrument track to an existing mix
  - 🔬 **Extract** — Isolate a stem from a mix
  - 🎹 **Complete** — Generate accompaniment for an existing track
- Multi-track timeline with per-track solo/mute/volume
- Persistent configuration via localStorage
- Batch generation support

---

## Requirements

- [ACE-Step 1.5](https://github.com/ace-step/ACE-Step-1.5) installed and running as an API server
- A modern browser (Chrome recommended)

---

## Install & Launch ACE-Step API Server

**1. Clone and install ACE-Step 1.5**

```bash
git clone https://github.com/ace-step/ACE-Step-1.5.git
cd ACE-Step-1.5
uv sync
```

**2. Launch the API server**

```bash
# Windows
start_api_server.bat

# Linux / macOS
uv run acestep-api
```

The server starts on `http://localhost:8001` by default.

---

## Download Models

**Standard models** are downloaded automatically on first run.

**XL BF16 models** (recommended for 16GB VRAM):

```bash
# XL Turbo BF16
huggingface-cli download marcorez8/acestep-v15-xl-turbo-bf16 --local-dir checkpoints/acestep-v15-xl-turbo-bf16

# XL Base BF16
huggingface-cli download marcorez8/acestep-v15-xl-base-bf16 --local-dir checkpoints/acestep-v15-xl-base-bf16
```

---

## Usage

1. Make sure the ACE-Step API server is running on `http://localhost:8001`
2. Open `acestep-studio.html` in your browser
3. Go to the **Service** tab, select your model and click **Initialize**
4. Start generating!

> **Base ★ modes** (Lego, Extract, Complete) require the Base model (`acestep-v15-base` or `acestep-v15-xl-base-bf16`).

---

## Credits

- [ACE-Step 1.5](https://github.com/ace-step/ACE-Step-1.5) by ACE Studio & StepFun
- XL BF16 models by [marcorez8](https://huggingface.co/marcorez8)
