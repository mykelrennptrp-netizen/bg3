---
id: RULES_DAMAGE_TYPES
name: Damage Types & Resistances Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Damage_types
logic_type: COMBAT_MATH_MODIFIER
---

# ☄️ Damage Types: v13.2 High-Fidelity Standard (Patch 8)

This node governs the elemental and physical damage interactions of all builds. It has been forensically satiated with the Octa-Matrix Standard, including **Resistances, Immunities, and Vulnerabilities**.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Damage Rules
> - **Vulnerability (SSoT)**: Target takes **2x** damage of that type.
> - **Resistance (SSoT)**: Target takes **0.5x** damage of that type (rounded down).
> - **Immunity (SSoT)**: Target takes **0** damage of that type.
> - **Physical Types**: Slashing, Piercing, Bludgeoning.

---

## 📊 Matrix A: Damage Interaction Mapping

| Damage_Type | Common Source | Magical Bypass Logic | Optimization |
| :--- | :--- | :--- | :--- |
| **RADIANT** | Cleric/Paladin | Automatically bypasses physical res. | **GOD (Synergy)** |
| **PSYCHIC** | Bard/Monk/GWM | Automatically bypasses physical res. | **S (Reliability)** |
| **LIGHTNING**| Sorcerer/Cleric | Automatically bypasses physical res. | **S (Burst)** |
| **COLD** | Wizard/Druid | Automatically bypasses physical res. | **S (Burst)** |
| **FORCE** | Warlock/Wizard | Automatically bypasses physical res. | **S (Static)** |
| **THUNDER** | Tempest/Bard | Automatically bypasses physical res. | **S (Control)** |
| **FIRE** | Sorcerer/Wizard | Automatically bypasses physical res. | **A (Burst)** |
| **ACID** | Rogue/Druid | Automatically bypasses physical res. | **B (Debuff)** |
| **NECROTIC** | Warlock/Wizard | Automatically bypasses physical res. | **B (Thematic)** |
| **PIERCING** | Rogue/Ranger | Requires +1 Weapon/Magical property. | **S (Martial)** |
| **SLASHING** | Fighter/Paladin | Requires +1 Weapon/Magical property. | **A (Martial)** |
| **BLUDGEON** | Monk/Barbarian | Requires +1 Weapon/Ki-Empowered. | **A (Martial)** |
| **POISON** | Rogue/Druid | Bypass res; Common Immunity. | **D (Risky)** |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "DAMAGE_TYPES_V13.2",
  "manifest_ref": "vanguard_manifest.json#ENGINE",
  "patch_baseline": "8_HOTFIX36",
  "multipliers": {
    "VULNERABLE": 2.0,
    "RESISTANT": 0.5,
    "IMMUNE": 0.0
  },
  "synergy_logic": {
    "WET_INTERACTION": {"COLD": 2.0, "LIGHTNING": 2.0, "FIRE": 0.5},
    "BREAD_AND_BUTTER": ["FORCE", "PSYCHIC", "RADIANT"]
  }
}
```
