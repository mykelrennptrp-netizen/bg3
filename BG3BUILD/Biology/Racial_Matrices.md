---
id: BIOLOGY_RACIAL_MATRICES
name: Unified Racial Forensic Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Races
logic_type: ATTRIBUTE_INJECTION
---

# 🧬 Racial Matrices: v13.2 High-Fidelity Standard (Patch 8)

This node governs the biological foundation of all builds. It has been forensically satiated with the Octa-Matrix Standard, including the **Patch 8 Flex-ASI** logic and sub-race mechanical pooling.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Racial Rules
> - **Flex-ASI (P8)**: All races now utilize the +2 / +1 allocation to ANY two distinct attributes.
> - **Movement (SSoT)**: Standard (9m) vs. Small (7.5m) vs. Wood Elf (10.5m).
> - **Darkvision**: Standard (12m) vs. Superior (24m).
> - **Weapon/Armor Proficiencies**: Racial proficiencies do **not** stack with class proficiencies; they "fill the gaps" for non-martial classes.

---

## 📊 Matrix A: Primary Racial Pools (Lv 1)

| Race_ID | Speed | Vision | Core_Forensic_Trait | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **GITHYANKI** | 9m | - | **Astral Knowledge**: Prof in all skills of a Stat. | **GOD_TIER (Utility)** |
| **WOOD_ELF** | 10.5m | 12m | **Fleet of Foot**: Highest base movement. | **S_TIER (Mobility)** |
| **HALF_ORC** | 9m | 12m | **Relentless Endurance**: Drop to 1 HP instead of 0. | **S_TIER (Sustain)** |
| **DUERGAR** | 7.5m | 24m | **Duergar Invisibility**: Infinite Invis (Out of Combat).| **S_TIER (Stealth)** |
| **DROW** | 9m | 24m | **Superior Darkvision** + Drow Magic (Faerie Fire).| **S_TIER (Caster)** |
| **GOLD_DWARF** | 7.5m | 12m | **Dwarven Toughness**: +1 Max HP per Level. | **A_TIER (Tank)** |
| **HIGH_ELF** | 9m | 12m | **High Cantrip**: Gain 1 Wizard Cantrip (INT based). | **A_TIER (Caster)** |
| **LIGHTFOOT** | 7.5m | 12m | **Naturally Stealthy**: Adv on Stealth checks. | **A_TIER (Rogue)** |
| **DEEP_GNOME** | 7.5m | 24m | **Gnome Cunning**: Adv on INT/WIS/CHA saves. | **A_TIER (Defense)** |
| **DRAGONBORN** | 9m | - | **Draconic Ancestry**: Breath Weapon + Resistance. | **B_TIER (Theme)** |
| **TIEFLING** | 9m | 12m | **Hellish Resistance**: Fire Damage Resistance. | **B_TIER (Tank)** |
| **HUMAN** | 9m | - | **Human Versatility**: +1 Skill Prof + Carry Capacity. | **C_TIER (Niche)** |

---

## 📈 Matrix C: Combat Trait Registry (Granular)

| Race_ID | Trait_ID | Type | Description | Optimization_Logic |
| :--- | :--- | :--- | :--- | :--- |
| **HALF_ORC** | **SAVAGE_ATT** | PASSIVE | Triple damage dice on Crits (Melee). | Best for Paladins/Barbarians. |
| **GITHYANKI** | **MISTY_STEP** | SPELL | Free Misty Step at Level 5. | Best mobility race for zero-cost. |
| **DUERGAR** | **ENLARGE** | SPELL | Free Enlarge (No Conc) at Level 5. | Massive DPR spike for martials. |
| **DROW** | **FAERIE_FIRE**| SPELL | Free Faerie Fire at Level 3. | Guaranteed Advantage for party. |
| **DWARF** | **DWAR_RESIL** | PASSIVE | Advantage on Poison Saves; Resistance Poison. | High defensive sustain. |
| **GITHYANKI** | **PSIONICS** | SPELL | Mage Hand (Invis) + Jump (Lv 3). | High tactical utility. |
| **GNOME**| **CUNNING** | PASSIVE | Adv on all Magic-based mental saves. | Top-tier defensive anchor. |
| **HALFLING** | **LUCKY** | PASSIVE | Reroll 1s on D20 rolls. | Mathematical floor protection. |

---

## 🎯 Matrix E: Weapon & Armour Pools (Forensic)

| Pool_ID | Prof_Gains | Impact |
| :--- | :--- | :--- |
| **CIVIL_MILIT** | Light Armour, Shield, Pike, Spear, Halberd, Glaive. | Essential for Sorcerer/Wizard/Bard AC. |
| **DROW_TRAIN** | Hand Crossbow, Rapier, Shortsword. | Grants Hand Xbow to non-Rogues. |
| **DWARVEN_COM** | Battleaxe, Handaxe, Light Hammer, Warhammer. | Strong for early-game Cleric/Druid melee. |
| **ELVEN_TRAIN** | Longsword, Shortsword, Longbow, Shortbow. | Grants Longbow to all classes. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "BIOLOGY_RACE_V13.2",
  "manifest_ref": "vanguard_manifest.json#BIOLOGY",
  "patch_baseline": "8_HOTFIX36",
  "ASI_logic": "FLEXIBLE_2_1_ALLOCATION",
  "optimization_priorities": {
    "versatility": "GITHYANKI",
    "stealth": "DUERGAR",
    "dpr_melee": "HALF_ORC",
    "dpr_ranged": "WOOD_ELF",
    "survivability": "DEEP_GNOME"
  },
  "subrace_overrides": {
    "Zariel_Tiefling": "Legacy_of_Avernus_Smites",
    "Gold_Dwarf": "Dwarven_Toughness_HP_Bonus",
    "Strongheart_Halfling": "Poison_Resilience"
  }
}
```
