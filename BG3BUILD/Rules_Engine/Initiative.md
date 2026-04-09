---
id: RULES_INITIATIVE
name: Initiative Rules Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Initiative
logic_type: TURN_ORDER_LOGIC
---

# ⚡ Initiative: v13.2 High-Fidelity Standard (Patch 8)

This node governs the turn order probability logic. It has been forensically satiated with the Octa-Matrix Standard, including the **BG3-specific 1d4 formula**.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Initiative Rules
> - **Formula (P8)**: `1d4 + DEX Mod + Initiative Bonuses`.
> - **Tie-Breaking (SSoT)**: Ties are resolved based on the character with the highest **DEX Score**. If still tied, it is random.
> - **Alert Feat**: Adds a flat **+5** to this roll, practically guaranteeing top-of-round actions.
> - **Surprised**: A character with the Surprised condition cannot take any actions or reactions on their first turn of combat.

---

## 📊 Matrix A: Initiative Scaling & Modifiers

| Source | Bonus | Formula Impact | wiki_Anchor |
| :--- | :--- | :--- | :--- |
| **DEX_MOD** | +1 per 2 dex| Primary scaling factor. | [Wiki](https://bg3.wiki/wiki/Initiative) |
| **ALERT_FEAT** | +5 | Massive flat bonus. | [Wiki](https://bg3.wiki/wiki/Alert) |
| **ELIXIR_VIGIL** | +5 | Long-rest elixir bonus. | [Wiki](https://bg3.wiki/wiki/Elixir_of_Vigilance) |
| **JAHEIRA_BOON** | +1d4 | Unique Origin permanent bonus. | [Wiki](https://bg3.wiki/wiki/Jaheira) |
| **SHIELD_THRALL**| +1 | Minor psionic bonus. | [Wiki](https://bg3.wiki/wiki/Illithid_powers) |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "INITIATIVE_V13.2",
  "manifest_ref": "vanguard_manifest.json#ENGINE",
  "patch_baseline": "8_HOTFIX36",
  "mechanics": {
    "dice_type": "1d4",
    "tie_breaker": "DEX_SCORE",
    "alert_bonus": 5,
    "surprised_modifier": "ACTION_LOSS"
  },
  "optimization_priorities": {
    "TOP_OF_ROUND": ["ALERT", "ELIXIR_OF_VIGILANCE", "HIGH_DEX"],
    "REACTION_DEFENSE": ["SHIELD", "COUNTERSPELL"]
  }
}
```
