<div align="center">
  <h1>🌌 Nebula</h1>
  <p><strong>The "Zero Bloat" Game Aggregator & Environment Orchestrator</strong></p>
</div>

## 🎯 The Vision

**Nebula** is a locally-driven, uncompromising game aggregator designed to decimate corporate launchers (Steam, GOG, Epic) in terms of performance and native Windows integration.

### Core Tenets
- ⚡ **Zero Bloat Performance**: Launch times measured in milliseconds.
- 🛡️ **Absolute Privacy**: Zero telemetry. 100% offline-first. Fully local database.
- ⚙️ **Deep OS Integration**: Hardware environment automation, Core Audio manipulation, and native file system orchestration.

## 🛠️ Technology Stack

Built for maximum efficiency using the modern web stack backed by bare-metal performance.

- **Framework**: [Tauri](https://tauri.app/) 
- **Backend**: Rust 🦀 (Native OS access, high-performance engines)
- **Frontend**: Vite + React/Svelte (Extremely fast, reactive UI)
- **Database**: SQLite (Relational cache-first architecture)

## 🧩 Core Architecture

The backend is modularized according to SOLID principles, handling heavy lifting while the frontend remains purely presentational.

### 1. Data Layer
All data relies on a local relational `SQLite` database (tables: *Platforms*, *Games*, *Installations*). It acts as a primary cache for network requests (e.g., pricing APIs), ensuring instant UI reactivity without disk polling.

### 2. The Core Engines
- 🔍 **Discovery Engine**: Uses the Strategy pattern to parse local manifests (Steam `.vdf`, Epic `JSON`) without altering original files.
- 🚀 **Execution Engine**: Leverages native URI Handlers (e.g., `steam://rungameid/[ID]`), offloading DRM and file verification to native clients.
- ⏱️ **Process Monitoring**: Zero-cost CPU play-time tracking via native Windows Event Tracing for process creation/termination.

## 🔮 Advanced System Modules

Nebula transcends basic cataloging by directly manipulating the Windows environment:

- 🎛️ **Hardware Profiles**: Win32 API orchestration to dynamically adjust monitor refresh rates, power plans, CPU Affinity Masks, and priority states per-game.
- 🎧 **Dynamic Audio Mixer**: Core Audio API (`IPolicyConfig`, `ISimpleAudioVolume`) integration for automatic device role-switching and background process muting during gameplay.
- 💾 **Save Game VCS**: A delta-copying version control system creating "decision trees" for game saves, allowing time-travel without massive storage overhead.

## 🔌 Integration Extensions
- **Local Screenshot OCR**: Asynchronous background text recognition (Tesseract) building a private, text-searchable screenshot database.
- **ITAD Promotions Engine**: Batch-queued integration with IsThereAnyDeal API to push native OS notifications when wishlisted games hit historical lows.

## 🚀 Getting Started

Ensure you have [Node.js](https://nodejs.org/), [Rust](https://www.rust-lang.org/) and the required build tools installed.

```bash
# Install dependencies
yarn install

# Run in development mode (Hot Reload for UI & Rust)
yarn tauri dev

# Build for production
yarn tauri build
```

---
*Built to take back control of your gaming library.*
