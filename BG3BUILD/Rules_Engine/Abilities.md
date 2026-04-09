---
id: RULES_ABILITIES
name: Abilities & Skill Proficiency Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Abilities
logic_type: ATTRIBUTE_MAPPING
---

# 📊 Abilities: v13.2 High-Fidelity Standard (Patch 8)

This node governs the core attributes and skills. It has been forensically satiated with the Octa-Matrix Standard, including **Ability Modifier Scaling** and **Skill Mapping**.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Ability Rules
> - **Modifier Formula (SSoT)**: `floor((Score - 10) / 2)`.
> - **Standard Array**: 15, 14, 13, 12, 10, 8.
> - **Point Buy**: 27 Points. Maximum base score of 15 (before racial ASI).
> - **Even Thresholds**: Only even numbers (12, 14, 16...) increase the modifier.

---

## 📊 Matrix A: Core Attributes & Scaling

| Ability | Full Name | Primary Scaling | Save Logic |
| :--- | :--- | :--- | :--- |
| **STR** | Strength | Melee Accuracy/Damage, Jump, Carry. | Physical Resistance |
| **DEX** | Dexterity | Finesse/Ranged, AC, Initiative. | Reflex/Dodging |
| **CON** | Constitution | HP (+1/lvl/mod), Concentration. | Stamina/Poison |
| **INT** | Intelligence | Wizard Casting, Investigation. | Mental (Illusion) |
| **WIS** | Wisdom | Cleric/Druid/Ranger Casting, Perception. | Mental (Control) |
| **CHA** | Charisma | Bard/Sorcerer/Lock/Paladin, Social. | Mental (Force/Self) |

---

## 🎭 Matrix B: Skill-to-Ability Mapping (Forensic)

| Skill | Ability | Optimization Goal |
| :--- | :--- | :--- |
| **ATHLETICS** | STR | Shove distance; Resist shove. |
| **ACROBATICS**| DEX | Resist shove; Reduce fall impact. |
| **STEALTH** | DEX | Hide from sight; Ambush. |
| **SLEIGHT_H** | DEX | Lockpicking; Pickpocketing; Disarm traps.|
| **ARCANA** | INT | Spell knowledge; Magical puzzles. |
| **HISTORY** | INT | Historical lore triggers. |
| **INVESTIG** | INT | Discovery of traps/details. |
| **NATURE** | INT | Animal/Plant knowledge. |
| **RELIGION** | INT | Divine knowledge; Mirror of Loss (DC 25). |
| **ANIMAL_H** | WIS | Train/Control animals. |
| **INSIGHT** | WIS | Detect lies/intent. |
| **MEDICINE** | WIS | Medical aid / stabilize. |
| **PERCEPTION** | WIS | Spot traps/secrets/ambush. |
| **SURVIVAL** | WIS | Tracking; Spotting buried treasure. |
| **DECEPTION** | CHA | Falsehoods; Social bypass. |
| **INTIMIDAT** | CHA | Forceful social bypass. |
| **PERFORM** | CHA | Musical instruments; Distraction. |
| **PERSUASION**| CHA | Peaceful social bypass; Price discount. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "ABILITIES_V13.2",
  "mechanics": {
    "modifier_logic": "floor((score-10)/2)",
    "point_buy_points": 27,
    "max_base_stat": 15
  },
  "skill_keys": {
    "STR": ["ATHLETICS"],
    "DEX": ["ACROBATICS", "STEALTH", "SLEIGHT_OF_HAND"],
    "INT": ["ARCANA", "HISTORY", "INVESTIGATION", "NATURE", "RELIGION"],
    "WIS": ["ANIMAL_HANDLING", "INSIGHT", "MEDICINE", "PERCEPTION", "SURVIVAL"],
    "CHA": ["DECEPTION", "INTIMIDATION", "PERFORMANCE", "PERSUASION"]
  }
}
```
