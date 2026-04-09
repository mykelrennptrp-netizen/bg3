---
id: RULES_DICE_ROLLS
name: Dice Roll Rules Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Dice_rolls
logic_type: COMBAT_LOGIC
---

# 🎲 Dice Roll Engine: v13.2 High-Fidelity Standard (Patch 8)

This node governs the core probability logic of the Vanguard Build Repository. It has been forensically satiated with the Octa-Matrix Standard, including **Patch 8 Automatic Success/Failure** logic.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Dice Rules
> - **Binary Criticals (SSoT)**: A Natural 20 is an automatic success on ALL d20 rolls (Attack, Saving Throw, Ability Check). A Natural 1 is an automatic failure.
> - **Critical Hit Threshold**: Default is 20. Can be reduced to 14-15 with specific gear/feature stacking.
> - **Damage Doubling**: Crits double all **Damage Dice** (including Smite/Sneak Attack) but **NOT** flat modifiers (+4 STR).
> - **Karmic Dice (User Setting)**: Agent must assume "Normal Distribution" (Off) unless specified.

---

## 📊 Matrix A: Roll Logic & Interactions

| State | Result | Logic_Forensic | wiki_Anchor |
| :--- | :--- | :--- | :--- |
| **ADVANTAGE** | Highest of 2 | `max(1d20, 1d20)` | [Wiki](https://bg3.wiki/wiki/Advantage) |
| **DISADVANTAGE**| Lowest of 2 | `min(1d20, 1d20)` | [Wiki](https://bg3.wiki/wiki/Disadvantage) |
| **CRIT_HIT** | Die Double | `(Dice * 2) + Mod` | [Wiki](https://bg3.wiki/wiki/Critical_Hit) |
| **SAVAGE_ATT** | Dice Reroll | Reroll damage dice; take highest. | [Wiki](https://bg3.wiki/wiki/Savage_Attacker) |
| **HALFLING_L** | Reroll Nat 1 | Automatic reroll on 1 (1st time only). | [Wiki](https://bg3.wiki/wiki/Luck_(Halfling_trait)) |
| **RELIABLE_T** | Min Roll 10 | If roll < 10, treat as 10 (Rogue 11). | [Wiki](https://bg3.wiki/wiki/Reliable_Talent) |

---

## 📈 Matrix C: Success Thresholds (Patch 8)

| Roll_Type | Natural_20 | Natural_1 | Automatic Scaling |
| :--- | :--- | :--- | :--- |
| **Attack** | **AUTO-HIT** | **AUTO-MISS** | Bypasses AC. |
| **Saving Throw**| **AUTO-PASS** | **AUTO-FAIL** | Bypasses DC. |
| **Ability Check**| **AUTO-PASS** | **AUTO-FAIL** | Bypasses Difficulty Class. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "DICE_ENGINE_V13.2",
  "manifest_ref": "vanguard_manifest.json#ENGINE",
  "patch_baseline": "8_HOTFIX36",
  "mechanics": {
    "dice_multiplier": 2,
    "advantage_stacking": "NON_STACKING_BINARY",
    "critical_threshold_min": 14,
    "savage_attacker_integration": "DICE_ONLY_REROLL"
  },
  "optimization_priorities": {
    "CRIT_FISHING": ["CHAMPION_3", "DEAD_SHOT", "SAREVOK_HELM"],
    "RELIABILITY": ["ADVANTAGE_STEADY_AIM", "ADVANTAGE_RISKY_RING"]
  }
}
```
