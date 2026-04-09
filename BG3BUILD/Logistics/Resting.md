---
id: LOGISTICS_RESTING
name: Resting & Recovery Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Resting
logic_type: RESOURCE_RECOVERY
---

# 🏕️ Resting: v13.2 High-Fidelity Standard (Patch 8)

This node governs the resource recovery logic for all builds. It has been forensically satiated with the Octa-Matrix Standard, including **Short vs. Long Rest** mechanical differentiation.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Resting Rules
> - **Short Rest (SSoT)**: Recover 50% HP + Short-Rest Resources (Pact Slots, Ki Points, Action Surge). Limit: **2 per Long Rest** (3 for Bards).
> - **Long Rest (SSoT)**: Recover 100% HP + All Resources + Spell Slots. Costs **40/80 Supplies** (Standard/Tactician+).
> - **Partial Long Rest**: Recover 50% HP/Slots if supplies are not met.

---

## 📊 Matrix A: Recovery Logic by Resource

| Resource_ID | Recovery_Trigger | Impact |
| :--- | :--- | :--- |
| **HP** | Short (50%) / Long (100%) | Vitality sustain. |
| **SPELL_SLOTS** | Long Rest (100%) | Primary caster limit. |
| **PACT_SLOTS** | Short Rest (100%) | Warlock-specific utility. |
| **KI_POINTS** | Short Rest (100%) | Monk-specific utility. |
| **ACT_SURGE** | Short Rest (100%) | Fighter-specific nova. |
| **DIV_CHANN** | Short Rest (100%) | Cleric/Paladin utility. |
| **SUP_DICE** | Short Rest (100%) | Battle Master utility. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "RESTING_V13.2",
  "manifest_ref": "vanguard_manifest.json#LOGISTICS",
  "patch_baseline": "8_HOTFIX36",
  "mechanics": {
    "short_rest_limit": 2,
    "bard_song_of_rest_bonus": 1,
    "long_rest_cost_tactician": 80,
    "long_rest_cost_balanced": 40
  },
  "recovery_mapping": {
    "SHORT_REST_OBJECTS": ["KI", "PACT_SLOTS", "ACTION_SURGE", "WILD_SHAPE", "BARDIC_INSP_LV5"],
    "LONG_REST_OBJECTS": ["WIZARD_SLOTS", "SORC_POINTS", "RAGE_CHARGES", "LUCK_POINTS"]
  }
}
```
