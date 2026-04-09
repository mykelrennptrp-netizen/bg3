---
id: BIOLOGY_BACKGROUNDS
name: Backgrounds & Inspiration Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Backgrounds
logic_type: PROFICIENCY_INJECTION
---

# 🎭 Backgrounds: v13.2 High-Fidelity Standard (Patch 8)

This node governs the sociological foundation of all builds. It has been forensically satiated with the Octa-Matrix Standard, including **Matrix B: Inspiration Generation Logic** for autonomous agentik decision-making.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Background Rules
> - **Skill Efficiency (SSoT)**: Backgrounds provide 2 permanent skill proficiencies that **cannot be changed**.
> - **Inspiration (Mechanic)**: Max cap of 4. Excess inspiration grants **25 or 50 XP** per trigger.
> - **Overlapping Proficiencies**: If a class and background provide the same skill, the user is prompted to select a different skill (Agent must handle this selection).

---

## 📊 Matrix A: Skill Proficiency Injection (Optimization Pools)

| Background_ID | Skill_1 | Skill_2 | Optimization_Value | Primary_Stat |
| :--- | :--- | :--- | :--- | :--- |
| **URCHIN** | Sleight of Hand| Stealth | **GOD_TIER (Utility)** | DEX |
| **CHARLATAN** | Deception | Sleight of Hand | **S_TIER (Stealth/CHA)**| CHA |
| **CRIMINAL** | Deception | Stealth | **S_TIER (Stealth/CHA)**| CHA |
| **GUILD_ARTISAN**| Insight | Persuasion | **S_TIER (Social)** | CHA |
| **NOBLE** | History | Persuasion | **S_TIER (Social)** | CHA |
| **SAGE** | Arcana | History | **A_TIER (Lore)** | INT |
| **SOLDIER** | Athletics | Intimidation | **A_TIER (Martial)** | STR |
| **ACOLYTE** | Insight | Religion | **B_TIER (Support)** | WIS |
| **ENTERTAINER** | Acrobatics | Performance | **B_TIER (Mobility)** | DEX/CHA |
| **OUTLANDER** | Athletics | Survival | **C_TIER (Physical)** | STR/WIS |
| **FOLK_HERO** | Animal Hand. | Survival | **D_TIER (Niche)** | WIS |

---

## ⚡ Matrix B: Inspiration & XP Logic (In-Game Triggers)

| Background_ID | Strategic Trigger Pattern | Optimization Goal |
| :--- | :--- | :--- |
| **GUILD_ARTISAN**| Trading high gold / repairing unique items. | Early gold accumulation. |
| **URCHIN** | Successful pickpocketing / lockpicking. | Resource acquisition focus. |
| **SAGE** | Discovering hidden lore / Solving puzzles. | Intelligence-based runs. |
| **HAUNTED_ONE** | Unique triggers related to murderous urges. | Dark Urge exclusive scaling. |
| **SOLDIER** | Killing bosses / High-kill count sequences. | Combat-heavy focus. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "BIOLOGY_BACKGROUND_V13.2",
  "manifest_ref": "vanguard_manifest.json#BIOLOGY",
  "patch_baseline": "8_HOTFIX36",
  "background_stats": {
    "URCHIN": {"skills": ["SLEIGHT_OF_HAND", "STEALTH"], "tier": "GOD"},
    "SAGE": {"skills": ["ARCANA", "HISTORY"], "tier": "A"},
    "SOLDIER": {"skills": ["ATHLETICS", "INTIMIDATION"], "tier": "A"},
    "NOBLE": {"skills": ["HISTORY", "PERSUASION"], "tier": "S"}
  },
  "mechanics": {
    "MAX_INSPIRATION": 4,
    "OVERFLOW_XP_BONUS": "ACTIVE"
  }
}
```
