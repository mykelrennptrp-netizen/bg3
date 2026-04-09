---
id: RULES_RESOURCES
name: Action Economy & Resource Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Resources
logic_type: ACTION_ECONOMY_LOGIC
---

# 🔋 Resources: v13.2 High-Fidelity Standard (Patch 8)

This node governs the Action Economy and expendable pools of all characters. It has been forensically satiated with the Octa-Matrix Standard, including **Bonus Action** and **Reaction** logic.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Resource Rules
> - **Standard Action (SSoT)**: Used for Spells, Attacks, Dash, Hide, etc. Most characters have 1.
> - **Bonus Action (SSoT)**: Used for Cunning Action, Spells (Misty Step), Off-hand Attacks. Most characters have 1 (Thief Rogues have 2).
> - **Reaction (SSoT)**: Used for Opportunity Attacks, Shield, Counterspell. Limit: **1 per Round**.
> - **Movement**: Measured in meters (9m base).

---

## 📊 Matrix A: Common Resource Pools

| Resource_ID | Base_Amount | Recovery | Primary Use |
| :--- | :--- | :--- | :--- |
| **ACTION** | 1 | Start of Turn | Main combat utility. |
| **BONUS_ACT** | 1 | Start of Turn | Secondary combat utility. |
| **REACTION** | 1 | Start of Round | Defensive/Triggered utility. |
| **Pact_Slot** | 1-3 | **Short Rest** | Warlock spellcasting. |
| **Spell_Slot** | Scaling | **Long Rest** | Standard spellcasting. |
| **Ki_Points** | Scaling | **Short Rest** | Monk features. |
| **Sorcery_Pts**| Scaling | **Long Rest** | Metamagic modifiers. |
| **SUP_DICE** | 4-6 | **Short Rest** | Battle Master Maneuvers. |
| **RAGE_CHARGE**| 2-6 | **Long Rest** | Barbarian Rage maintenance. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "RESOURCES_V13.2",
  "manifest_ref": "vanguard_manifest.json#ENGINE",
  "patch_baseline": "8_HOTFIX36",
  "action_economy": {
    "action_standard": 1,
    "bonus_action_standard": 1,
    "reaction_per_round": 1,
    "extra_attack_stacking": "NON_STACKING_HM"
  },
  "resource_recovery": {
    "SHORT_REST": ["KI", "PACT_SLOTS", "ACTION_SURGE", "CHANNEL_DIVINITY"],
    "LONG_REST": ["SPELL_SLOTS", "SORCERY_POINTS", "LUCK_POINTS"]
  }
}
```
