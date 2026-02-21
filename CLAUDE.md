# CLAUDE.md — AI Assistant Guide for MyWorld

## Project Overview

**MyWorld (마이월드)** is a 2D top-down RPG web game inspired by Minecraft, built as an educational project with children (ages 8+). The game features a village hub, field exploration, turn-based combat, item crafting, and character progression — all rendered with emoji-based graphics and Korean UI.

**Status**: Early prototype (v0.1). Game systems are designed and documented in `claude.md`, but the full game code has not yet been implemented in `index.html`.

## Repository Structure

```
myworld/
├── index.html    # Game entry point (HTML + CSS + JS, single-file architecture)
├── claude.md     # Game design document (Korean) — systems, stats, recipes, roadmap
├── README.md     # Brief project introduction
└── CLAUDE.md     # This file — AI assistant guidance
```

There are no subdirectories, build configs, or dependency files. The entire project lives in these files.

## Technology Stack

| Layer      | Technology             |
|------------|------------------------|
| Rendering  | HTML5 Canvas           |
| Logic      | Vanilla JavaScript     |
| Styling    | CSS3                   |
| Deployment | GitHub Pages (static)  |

**No external dependencies.** No npm, no bundler, no framework. Pure web technologies only.

## Development Workflow

### Running Locally

Open `index.html` directly in a browser. No build step, no dev server required.

### Deployment

Static hosting via GitHub Pages. The `index.html` file is served as-is.

### Testing

No test framework is configured. Verify changes by opening `index.html` in a browser and manually testing game functionality.

### Linting / Formatting

No automated linting or formatting tools are configured. Follow the conventions described below.

## Architecture & Key Decisions

### Single-File Architecture

All game code (HTML structure, CSS styles, JavaScript logic) goes into `index.html`. This is intentional:
- Simplifies deployment (one file to host)
- Makes sharing easy (copy one file)
- Appropriate for the project's scope and educational purpose

Do **not** split the project into multiple files unless explicitly requested.

### Emoji-Based Graphics

The game uses emoji characters for all visual elements (characters, monsters, items, buildings). Do not introduce sprite sheets, image assets, or external graphic libraries unless requested.

### Game Design Document

`claude.md` (lowercase) is the authoritative game design reference. It contains:
- Character stats and level-up formulas
- Village building descriptions
- Field regions with level requirements and monster tables
- Combat mechanics
- Crafting recipes with exact material costs
- Development roadmap (Phase 1–4)

Always consult `claude.md` when implementing game features to ensure consistency with the design spec.

## Coding Conventions

### Language

- **UI text**: Korean (한국어). All in-game strings, labels, and messages must be in Korean.
- **Code**: Variable names, function names, and comments may use English.

### Style Guidelines

- Keep all game code within `index.html`
- Use semantic, descriptive variable and function names
- Organize JavaScript into clear sections (game state, rendering, input handling, combat, crafting, etc.)
- Prefer readability over cleverness — this is an educational project
- Use emoji constants for visual elements (e.g., `const PLAYER_BOY = '🧒'`)

### Git Conventions

- Write clear, descriptive commit messages in English
- Keep commits focused on a single change or feature

## Game Systems Reference (Quick Summary)

Detailed specs are in `claude.md`. Key parameters for implementation:

- **Level-up**: HP +15, ATK +2, DEF +1 per level
- **4 field regions**: Meadow (Lv1+), Forest (Lv3+), Mountain (Lv5+), Dragon's Cave (Lv8+)
- **7 crafting recipes** with specific material requirements
- **Turn-based combat**: Attack / Recover / Escape actions
- **Shop items**: Apple (10G), Meat (25G), Potion (60G), Herb (15G)
- **Input**: Arrow keys + touch D-Pad support

## What Needs to Be Done

The `index.html` currently contains only a placeholder. The primary next step is implementing the full game as described in `claude.md`, following the Phase 1 checklist:

- [x] Character selection & village (designed)
- [x] Field exploration & combat (designed)
- [x] Items & crafting (designed)
- [x] Level-up system (designed)
- [ ] **Full game code implementation in `index.html`**

## Guidelines for AI Assistants

1. **Read `claude.md` first** before implementing any game feature — it is the single source of truth for game design.
2. **Maintain single-file architecture** — all code stays in `index.html`.
3. **Use Korean for all player-facing text.** Code internals can be English.
4. **Use emoji for graphics.** No external image assets.
5. **Keep it simple.** The target audience is children. Avoid complex abstractions.
6. **No external dependencies.** Do not add npm packages, CDN scripts, or frameworks.
7. **Preserve existing design decisions** documented in `claude.md` (stat values, recipes, monster tables, etc.) unless the user explicitly asks for changes.
8. **Test by opening `index.html` in a browser.** There is no automated test suite.
