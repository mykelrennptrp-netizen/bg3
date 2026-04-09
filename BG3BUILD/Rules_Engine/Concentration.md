---
id: RULES_CONCENTRATION
name: Concentration & Maintenance Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Concentration
logic_type: MAINTENANCE_LOGIC
---

# 🧠 Concentration: v13.2 High-Fidelity Standard (Patch 8)

This node governs the maintenance logic of persistent magical effects. It has been forensically satiated with the Octa-Matrix Standard, including **Break Triggers** and **War Caster** optimization.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Concentration Rules
> - **Binary Limit**: A character can only concentrate on ONE spell at a time.
> - **The Save (SSoT)**: When taking damage, the character must pass a CON Saving Throw. DC = 10 or half the damage taken (whichever is higher).
> - **Incapacitation**: Conditions like *Prone*, *Stunned*, or *Paralyzed* immediately end Concentration.
> - **Shadow Blade (P8)**: Shadow Blade is the primary exception in Patch 8; it **no longer requires concentration**.

---

## 📊 Matrix A: High-Value Concentration Spells (v13.2)

| Spell_ID | Impact | Vulnerability | Optimization_Cap |
| :--- | :--- | :--- | :--- |
| **HASTE** | Massive (2 Actions). | Lethargic (Turn Loss) if broken. | **S_TIER (Risky)** |
| **HOLD_MONSTER**| Boss Shutdown. | High Boss DPR can break save. | **S_TIER (Control)** |
| **SPIRIT_GUAR** | AOE DOT + Slow. | Frontline exposure increases checks. | **GOD_TIER (Cleric)** |
| **BLESS** | Global hit chance. | Low level slots; easy to recast. | **S_TIER (Buff)** |
| **GLOBE_INVUL** | Damage Immunity. | Requires static position. | **GOD_TIER (Def)** |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "CONCENTRATION_V13.2",
  "manifest_ref": "vanguard_manifest.json#ENGINE",
  "patch_baseline": "8_HOTFIX36",
  "mechanics": {
    "save_dc_base": 10,
    "save_dc_dmg_ratio": 0.5,
    "break_conditions": ["PRONE", "STUNNED", "PARALYZED", "SLEEPING", "INCAPACITATED"]
  },
  "synergy_mapping": {
    "MAINTENANCE_GOD": ["WAR_CASTER_ADV", "RESILIENT_CON", "PEERLESS_FOCUS_ELIXIR"],
    "UNBREAKABLE_INIT": ["GLOBE_OF_INVULNERABILITY", "CON_23_AMULET"]
  }
}
```
