# BG3 Antigravity Theorycrafting Lab

> AI-grounded workspace for Baldur's Gate 3 character build creation, min-maxing, and optimization.

## Overview

This workspace is designed for the **Antigravity IDE** (Google App) to provide an AI-powered theorycrafting environment for Baldur's Gate 3. It is grounded to authoritative data sources to ensure accurate, verifiable build recommendations.

## Data Sources

| Priority | Source | Type | Description |
|----------|--------|------|-------------|
| **Primary** | `BG3BUILD/` Data Hub | Local | Forensic data repository (Octa-Matrix v13.2, Patch 8 HF36) containing all game mechanics, classes, equipment, and optimization matrices |
| **Secondary** | [bg3.wiki](https://bg3.wiki/) | Web | Community wiki for supplementary lookups, item locations, and edge-case verification |

> **Grounding Policy:** The data hub is the authoritative source. The wiki is supplementary. On conflicts, data hub values take precedence.

## Workspace Structure

```
workspace/
├── workspace.json              # Main workspace manifest & grounding config
├── system_instructions.md      # AI agent system prompt & build protocol
├── templates/
│   └── build_template.json     # Structured schema for build definitions
├── builds/                     # Saved build files (user-created)
└── README.md                   # This file
```

## Quick Start

### 1. Open in Antigravity IDE

Load this workspace by pointing Antigravity IDE to the repository root. The workspace manifest at `workspace/workspace.json` defines all data source grounding and project configuration.

### 2. Configure Grounding

The workspace is pre-configured with:
- **Primary grounding** to the `BG3BUILD/` data hub (all local `.md` and `.json` files)
- **Secondary grounding** to `https://bg3.wiki/` for web-based supplementary data

### 3. Start Building

Ask the agent to create a build. Example prompts:

- *"Create a Honour Mode Swords Bard / Paladin multiclass build focused on melee DPR."*
- *"What's the optimal ability score spread for a Gloom Stalker Ranger / Assassin Rogue?"*
- *"Compare a pure Fighter Champion vs a Fighter 5 / Barbarian 7 Wildheart for tanking."*
- *"Build me a GOD-tier Sorcerer / Warlock for maximum Eldritch Blast damage."*

### 4. Save Builds

Completed builds are saved as JSON files in `workspace/builds/` using the template schema from `workspace/templates/build_template.json`.

## Data Hub Coverage

The BG3BUILD data hub covers:

| Domain | Files | Scope |
|--------|-------|-------|
| Biology | 3 | Races, Backgrounds, Origins |
| Disciplines | 16 | 12 Classes, Feats, Master Manifest |
| Rules Engine | 11 | Abilities, AC, Dice, Proficiency, Resources, Honour Mode |
| Library | 11 | Spells, Weapons, Armor, Accessories, Alchemy, Conditions |
| Logic | 1 | Multiclassing rules & spell slot calculations |
| Logistics | 2 | Rest mechanics, Inspiration economy |

**Total: 44 structured files + 1 JSON manifest**

## Build Protocol

Every build follows an 8-step protocol (detailed in `system_instructions.md`):

1. **Define Build Identity** — Name, mode, role, class structure
2. **Race & Background** — Racial traits, proficiency matching
3. **Ability Scores** — Point Buy / Standard Array optimization
4. **Class Progression** — Level 1–12 feature mapping
5. **Feat Selection** — Optimization-tiered feat picks at 4/8/12
6. **Equipment Loadout** — Weapon, armor, and accessory synergies
7. **Spell Selection** — Tier-rated spell picks, concentration management
8. **Optimization Analysis** — DPR, AC, HP, resource economy, tier rating

## Tier System

All optimization ratings use the standard tier system:

| Tier | Meaning |
|------|---------|
| **GOD** | Best-in-slot, meta-defining |
| **S** | Exceptional, top-tier choice |
| **A** | Strong, reliable pick |
| **B** | Good, situationally optimal |
| **C** | Average, functional |
| **D** | Weak, generally suboptimal |
