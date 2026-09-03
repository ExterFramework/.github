<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00e676,50:00c853,100:0d1117&height=180&section=header&text=ExterFramework&fontSize=64&fontColor=ffffff&fontAlignY=40" width="100%"/>
</div>

# ExterFramework

ExterFramework is a modular resource ecosystem for FiveM server development. It provides a set of interoperable Lua resources and NUI applications covering core infrastructure, UI primitives, HUD components, in-game applications, and gameplay systems. Resources share a common event and utility layer (`exter-lib`) so that individual modules can be adopted independently or combined into a full server build.

Repositories: https://github.com/orgs/ExterFramework/repositories
Maintainer: https://github.com/SOBING4413

---

## Module Reference

### Core Infrastructure

| Module | Description | Stack |
|---|---|---|
| exter-lib | Shared utility library providing the framework bridge layer, event abstractions, callback handling, and helper functions used by all other modules. | Lua, JS, HTML, CSS |
| exter-loading | Loading screen with progress tracking and asset preloading. | HTML, CSS, JS |
| exter-spawn | Spawn selection, last-position recall, and new-character onboarding. | Lua, NUI |

### UI Primitives

| Module | Description | Stack |
|---|---|---|
| exter-notify | Toast notification engine with configurable position, duration, and type. | Lua, React, TypeScript |
| exter-drawtext | On-screen text overlay for contextual instructions and key prompts. | Lua, NUI |
| exter-progressbar | Asynchronous progress indicator supporting cancellation and bar/circle variants. | Lua, React, TypeScript |
| exter-input | Form dialog generator supporting text, number, select, checkbox, and slider inputs. | Lua, React, TypeScript |
| exter-menu | Scrollable list menu with headers, descriptions, icons, and nested sub-menus. | Lua, React, TypeScript |
| exter-context | Interaction-triggered context menu with nested items. | Lua, React, TypeScript |
| exter-radial | Circular menu for quick-access actions. | Lua, React, TypeScript |
| exter-target | Raycast-based entity and zone targeting with contextual options. | Lua, React, TypeScript |

### HUD and Interface Systems

| Module | Description | Stack |
|---|---|---|
| exter-hud | Player HUD displaying health, armor, hunger, thirst, stress, and vehicle speedometer. | Lua, HTML, CSS, JS |
| exter-scoreboard | Server player list with ping, identifier, and job information. | Lua, React, TypeScript |
| exter-chat | Chat system with command handling and message formatting. | Lua, NUI |
| exter-dispatch | Dispatch system for job alerts and response coordination. | Lua, React, TypeScript |

### Application Modules

| Module | Description | Stack |
|---|---|---|
| exter-phone | Smartphone interface with calls, messages, contacts, camera, and settings applications. | Lua, React, TypeScript |
| exter-laptop | Computer interface with browser and application support. | Lua, React, TypeScript |
| exter-admin | Administration panel for player management, moderation actions, and entity control. | Lua, React, TypeScript |
| exter-multicharacter | Character slot system with creation, selection, and deletion. | Lua, React, TypeScript |

### Gameplay Systems

| Module | Description | Stack |
|---|---|---|
| exter-inventory | Drag-and-drop inventory with weight and slot management, item metadata, and crafting hooks. | Lua, React, TypeScript |
| exter-banking | Account management, transaction history, transfers, and ATM interface. | Lua, React, TypeScript |
| exter-garage | Vehicle storage, retrieval, and impound handling. | Lua, React, TypeScript |
| exter-vehicleshop | Vehicle catalog, test drives, and purchase flow. | Lua, React, TypeScript |
| exter-housing | Property ownership, interior management, key sharing, and stash storage. | Lua, React, TypeScript |
| exter-clothing | Outfit and accessory management. | Lua, React, TypeScript |
| exter-doorlock | Door and gate access control with lockpicking and job-based permissions. | Lua, NUI |
| exter-weathersync | Weather and time synchronization with administrative overrides. | Lua |
| exter-racingapp | Race creation, checkpoints, leaderboards, and betting. | Lua, React, TypeScript |

### Job Systems

| Module | Description | Stack |
|---|---|---|
| exter-policejob | Duty management, evidence handling, restraint mechanics, and vehicle impound. | Lua, NUI |
| exter-ambulancejob | Revive mechanics, stretcher handling, and hospital check-in. | Lua, NUI |

---

## Technology Stack

| Layer | Technology |
|---|---|
| Game logic | Lua (server and client scripting for FiveM) |
| NUI frontend | React, TypeScript, Tailwind CSS |
| Legacy NUI | HTML, CSS, JavaScript |
| Build tooling | Vite, pnpm |
| Runtime | FiveM (CFX platform) |
| Database | MySQL / MariaDB via oxmysql |

---

## Requirements

- A FiveM server (cfx.re), configured via txAdmin or manual setup
- Node.js 18 or later, and pnpm, for building NUI frontends
- oxmysql as the database driver
- A supported framework bridge (QBCore or compatible)

## Installation

```bash
# Clone the required modules into the server's resources directory
git clone https://github.com/ExterFramework/exter-lib.git [resources]/exter-lib
git clone https://github.com/ExterFramework/exter-hud.git [resources]/exter-hud
# repeat for each additional module

# Build the NUI frontend for modules that ship a React/TypeScript interface
cd [resources]/exter-hud/web
pnpm install
pnpm build
```

Add the modules to `server.cfg` in dependency order:

```
ensure exter-lib
ensure exter-hud
ensure exter-notify
# additional modules
```

### Dependency Order

```
exter-lib                          required by all other modules
  UI primitives                    no inter-module dependencies
  exter-spawn                   -> exter-multicharacter
  exter-inventory                -> exter-clothing, exter-housing
  exter-policejob / exter-ambulancejob -> exter-dispatch
```

---

## Repository Statistics

| Metric | Value |
|---|---|
| Repositories | 42+ |
| Primary language | Lua |
| NUI stack | React, TypeScript |
| Module categories | 6 (core, UI, HUD, applications, gameplay, jobs) |
| Contributions (trailing 12 months) | 798+ |
| Pull requests (April 2026) | 77+ across 38 repositories |
| Commits (April 2026) | 469+ across 64 repositories |

---

## Design Principles

- **Modularity** — each resource is self-contained; server operators adopt only the modules they need.
- **Interoperability** — a shared event contract in `exter-lib` standardizes communication between modules.
- **Server-authoritative logic** — critical game mechanics are validated server-side to reduce client-side exploitation.
- **Consistent frontend stack** — UI modules use React and TypeScript with Tailwind CSS, with Vite providing hot-reload during development.
- **Consistent API conventions** — event names, exports, and configuration patterns follow the same structure across modules to reduce integration overhead.

---

## Contributing

1. Fork the target repository.
2. Create a feature branch: `git checkout -b feat/your-feature`.
3. Commit using conventional commit messages: `git commit -m "feat: add your feature"`.
4. Push the branch and open a pull request describing the change, its motivation, and any breaking changes.

Contributions should follow the existing code style and include documentation updates where applicable.

---

## Maintainer

**SOBING4413** — https://github.com/SOBING4413

Sole maintainer and architect of the ExterFramework ecosystem.

---

## License

ExterFramework modules are open source. License terms are specified per repository; consult the `LICENSE` file in each module before use or redistribution.
