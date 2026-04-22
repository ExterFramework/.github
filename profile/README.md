<div align="center">

<!-- Header Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00e676,50:00c853,100:0d1117&height=200&section=header&text=ExterFramework&fontSize=80&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Next-Generation%20FiveM%20%26%20Roblox%20Development%20Ecosystem&descAlignY=55&descSize=18" width="100%"/>

<br/>

<!-- Badges -->
![Repositories](https://img.shields.io/badge/Repositories-42+-00e676?style=for-the-badge&logo=github&logoColor=white)
![Language](https://img.shields.io/badge/Primary-Lua-2C2D72?style=for-the-badge&logo=lua&logoColor=white)
![TypeScript](https://img.shields.io/badge/Frontend-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![FiveM](https://img.shields.io/badge/Platform-FiveM-F40552?style=for-the-badge&logo=fivem&logoColor=white)
![Roblox](https://img.shields.io/badge/Platform-Roblox-000000?style=for-the-badge&logo=roblox&logoColor=white)
![License](https://img.shields.io/badge/License-Open%20Source-00c853?style=for-the-badge&logo=opensourceinitiative&logoColor=white)

<br/>

> **⚡ A modular, production-grade framework ecosystem engineered for high-performance game server development.**

🌐 [Website](https://exterframeworked.gt.tc/) • 📦 [Repositories](https://github.com/orgs/ExterFramework/repositories) • 👤 [Creator](https://github.com/SOBING4413)

---

</div>

## 📖 Overview

**ExterFramework** is a comprehensive, open-source development ecosystem purpose-built for **FiveM** (GTA V multiplayer) and **Roblox** game server environments. The framework provides a complete suite of interconnected modules — from core UI primitives and HUD systems to full-featured gameplay mechanics — designed with a modular architecture that enables server operators to deploy production-ready features with minimal configuration overhead.

Built primarily in **Lua** (server/client game logic) and **TypeScript/React** (NUI web interfaces), ExterFramework follows a consistent design philosophy: each module is self-contained yet interoperable, communicating through a shared library layer (`exter-lib`) that standardizes event handling, state management, and cross-resource communication.

---

## 🏗️ Architecture

```
ExterFramework/
├── 🔧 Core Infrastructure
│   ├── exter-lib            # Shared library — event bus, utilities, bridge layer
│   ├── exter-loading        # Client bootstrap & asset loading screen
│   └── exter-spawn          # Character spawn orchestration & session init
│
├── 🎨 UI Primitives (NUI Components)
│   ├── exter-notify         # Toast notification system
│   ├── exter-drawtext       # On-screen instructional text renderer
│   ├── exter-progressbar    # Async progress bar with cancellation support
│   ├── exter-input          # Dynamic form input dialogs
│   ├── exter-menu           # Navigable list menu system
│   ├── exter-context        # Context menu (right-click) interface
│   ├── exter-radial         # Radial/pie menu for quick actions
│   └── exter-target         # 3D world-space targeting (eye/interaction)
│
├── 🖥️ HUD & Interface Systems
│   ├── exter-hud            # Player HUD — health, armor, hunger, thirst, etc.
│   ├── exter-scoreboard     # Server player list & scoreboard
│   ├── exter-chat           # In-game chat system with commands
│   └── exter-dispatch       # Emergency dispatch & alert system
│
├── 📱 Application Modules
│   ├── exter-phone          # In-game smartphone with apps ecosystem
│   ├── exter-laptop         # In-game laptop/computer interface
│   ├── exter-admin          # Server administration panel
│   └── exter-multicharacter # Multi-character selection & management
│
├── 🎮 Gameplay Systems
│   ├── exter-inventory      # Item inventory with drag-and-drop
│   ├── exter-banking        # Banking system — accounts, transfers, ATM
│   ├── exter-garage         # Vehicle garage & impound management
│   ├── exter-vehicleshop    # Vehicle dealership & purchasing
│   ├── exter-housing        # Property ownership & interior management
│   ├── exter-clothing       # Character clothing & outfit system
│   ├── exter-doorlock       # Door lock/unlock & access control
│   ├── exter-racingapp      # Street racing with leaderboards
│   └── exter-weathersync    # Dynamic weather & time synchronization
│
├── 👮 Job Systems
│   ├── exter-policejob      # Law enforcement job framework
│   └── exter-ambulancejob   # EMS/paramedic job framework
│
└── 🎯 Roblox Modules
    ├── GUI                  # Roblox GUI framework (TypeScript)
    └── [Various Scripts]    # Roblox Lua game scripts & utilities
```

---

## 🧩 Module Catalog

### Core Infrastructure

| Module | Description | Stack |
|--------|-------------|-------|
| **exter-lib** | Shared utility library providing the bridge layer, event abstractions, callback system, and common helper functions used across all modules | `Lua` |
| **exter-loading** | Customizable loading screen with progress tracking, asset preloading, and server branding | `HTML` `CSS` `JS` |
| **exter-spawn** | Spawn selection system with location management, last-position recall, and new-character onboarding flow | `Lua` `NUI` |

### UI Primitives

| Module | Description | Stack |
|--------|-------------|-------|
| **exter-notify** | Non-blocking toast notification engine with configurable position, duration, type (success/error/info/warning), and animation | `Lua` `React` `TS` |
| **exter-drawtext** | Lightweight on-screen text overlay for contextual instructions and key prompts | `Lua` `NUI` |
| **exter-progressbar** | Asynchronous progress indicator with label, duration, cancellation, and animation variants (bar/circle) | `Lua` `React` `TS` |
| **exter-input** | Dynamic form dialog generator supporting text, number, select, checkbox, slider, and color inputs | `Lua` `React` `TS` |
| **exter-menu** | Scrollable list menu with header, description, icons, and nested sub-menus | `Lua` `React` `TS` |
| **exter-context** | Context-sensitive menu triggered by interaction, supporting nested items and icons | `Lua` `React` `TS` |
| **exter-radial** | Circular/pie menu for quick-access actions with customizable segments and icons | `Lua` `React` `TS` |
| **exter-target** | 3D world-space interaction system — raycast-based entity/zone targeting with contextual options | `Lua` `React` `TS` |

### Application & Gameplay Modules

| Module | Description | Stack |
|--------|-------------|-------|
| **exter-phone** | Full-featured smartphone with apps (calls, messages, contacts, camera, settings) | `Lua` `React` `TS` |
| **exter-laptop** | In-game computer interface with browser and application support | `Lua` `React` `TS` |
| **exter-inventory** | Drag-and-drop inventory system with weight/slot management, item metadata, and crafting hooks | `Lua` `React` `TS` |
| **exter-banking** | Complete banking system — checking/savings accounts, transfers, transaction history, ATM interface | `Lua` `React` `TS` |
| **exter-garage** | Vehicle storage, retrieval, and impound management with garage location support | `Lua` `React` `TS` |
| **exter-vehicleshop** | Vehicle dealership with catalog browsing, test drives, and purchase flow | `Lua` `React` `TS` |
| **exter-housing** | Property system with ownership, interior decoration, key sharing, and stash storage | `Lua` `React` `TS` |
| **exter-clothing** | Character customization — outfits, accessories, wardrobe management | `Lua` `React` `TS` |
| **exter-racingapp** | Street racing system with race creation, checkpoints, leaderboards, and betting | `Lua` `React` `TS` |
| **exter-admin** | Server administration panel — player management, bans, teleportation, entity spawning | `Lua` `React` `TS` |
| **exter-multicharacter** | Multi-character slot system with character creation, selection, and deletion | `Lua` `React` `TS` |
| **exter-dispatch** | Emergency dispatch system for job alerts, GPS tracking, and response coordination | `Lua` `React` `TS` |
| **exter-doorlock** | Door/gate access control with lockpicking, key items, and job-based permissions | `Lua` `NUI` |
| **exter-weathersync** | Server-wide weather and time synchronization with admin overrides | `Lua` |
| **exter-hud** | Player HUD displaying health, armor, hunger, thirst, stress, and vehicle speedometer | `Lua` `React` `TS` |
| **exter-scoreboard** | Server player list with ping, ID, job info, and admin tools | `Lua` `React` `TS` |
| **exter-chat** | In-game chat with command system, channels, and message formatting | `Lua` `NUI` |
| **exter-policejob** | Police job framework — duty toggle, evidence, cuffing, vehicle impound | `Lua` `NUI` |
| **exter-ambulancejob** | EMS job framework — revive mechanics, stretcher, hospital check-in | `Lua` `NUI` |

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technologies |
|-------|-------------|
| **Game Logic** | ![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white) — Server & client-side scripting (FiveM/Roblox) |
| **NUI Frontend** | ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) |
| **Build Tools** | ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) ![pnpm](https://img.shields.io/badge/pnpm-F69220?style=flat-square&logo=pnpm&logoColor=white) |
| **Runtime** | ![FiveM](https://img.shields.io/badge/CFX/FiveM-F40552?style=flat-square) ![Roblox](https://img.shields.io/badge/Roblox_Studio-000000?style=flat-square&logo=roblox&logoColor=white) |
| **Database** | ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) / ![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white) via oxmysql |

</div>

---

## 🚀 Quick Start

### Prerequisites

- **FiveM Server** — [cfx.re](https://cfx.re/) with txAdmin or manual setup
- **Node.js** ≥ 18.x & **pnpm** — for building NUI frontends
- **oxmysql** — database driver resource
- **QBCore** or compatible framework bridge

### Installation

```bash
# 1. Clone the desired module(s) into your server resources
git clone https://github.com/ExterFramework/exter-lib.git [resources]/exter-lib
git clone https://github.com/ExterFramework/exter-hud.git [resources]/exter-hud
# ... repeat for each module

# 2. Build NUI frontends (for modules with React/TS interfaces)
cd [resources]/exter-hud/web
pnpm install
pnpm build

# 3. Add to your server.cfg
ensure exter-lib        # Always load the shared library first
ensure exter-hud
ensure exter-notify
# ... add remaining modules in dependency order
```

### Module Dependency Order

```
exter-lib (REQUIRED — load first)
  └── All other exter-* modules depend on exter-lib
      ├── UI Primitives (no inter-dependencies)
      ├── exter-spawn → exter-multicharacter
      ├── exter-inventory → exter-clothing, exter-housing
      └── exter-policejob / exter-ambulancejob → exter-dispatch
```

---

## 📊 Project Statistics

<div align="center">

| Metric | Value |
|--------|-------|
| **Total Repositories** | 42+ |
| **Primary Language** | Lua |
| **NUI Stack** | React + TypeScript |
| **Module Categories** | 6 (Core, UI, HUD, Apps, Gameplay, Jobs) |
| **Active Development** | ✅ 798+ contributions (last 12 months) |
| **Pull Requests (Apr 2026)** | 77+ across 38 repositories |
| **Commits (Apr 2026)** | 469+ across 64 repositories |

</div>

---

## 🎨 Design Philosophy

- **🧱 Modularity** — Each resource is a standalone module. Pick only what you need; no monolithic dependencies.
- **🔌 Interoperability** — Standardized event contracts via `exter-lib` ensure modules communicate seamlessly.
- **🎭 Modern NUI** — All UI modules leverage React + TypeScript with Tailwind CSS for responsive, performant in-game interfaces.
- **⚡ Performance-First** — Lua-side logic is optimized for minimal tick overhead; NUI communication uses targeted message passing.
- **🔒 Security** — Server-authoritative design patterns prevent client-side exploitation of critical game mechanics.
- **🎯 Developer Experience** — Consistent API patterns, typed interfaces, and hot-reload support via Vite during NUI development.

---

## 🤝 Contributing

We welcome contributions from the community. Whether it's bug fixes, new features, or documentation improvements:

1. **Fork** the target repository
2. **Create** a feature branch (`git checkout -b feat/your-feature`)
3. **Commit** with conventional commits (`git commit -m "feat: add new feature"`)
4. **Push** to your fork (`git push origin feat/your-feature`)
5. **Open** a Pull Request with a clear description of changes

Please ensure your code follows the existing style conventions and includes appropriate documentation.

---

## 👨‍💻 Creator & Maintainer

<div align="center">

<a href="https://github.com/SOBING4413">
  <img src="https://avatars.githubusercontent.com/u/194123481?v=4" width="120" style="border-radius: 50%;" alt="SOBING4413"/>
</a>

### **SOBING4413**

*Lead Developer & Framework Architect*

[![GitHub](https://img.shields.io/badge/GitHub-SOBING4413-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SOBING4413)

> Full-stack game developer specializing in FiveM resource development and Roblox scripting. Creator and sole maintainer of the ExterFramework ecosystem with 798+ contributions across 42+ repositories.

</div>

---

## 📜 License

ExterFramework modules are open-source. Individual repositories may specify their own license terms — please refer to each module's `LICENSE` file for details.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00e676,50:00c853,100:0d1117&height=120&section=footer" width="100%"/>

<sub>Built with 💚 by the ExterFramework community</sub>

<br/>

![Visitors](https://komarev.com/ghpvc/?username=ExterFramework&style=for-the-badge&color=00c853&label=PROFILE+VIEWS)

</div>
