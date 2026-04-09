---
id: LIBRARY_ILLITHID_POWERS
name: Illithid Forensic Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Illithid_powers
logic_type: MECHANICAL_ABSTRACTION
---

# 🧠 Illithid Powers: v13.2 High-Fidelity Standard (Patch 8)

This node governs the psionic overlays that augment character builds. It has been forensically satiated with the **Full Pool of 26 Powers** for Gemini Pro build architecture.

---

## 📊 Matrix A: Tier 1 & 2 Powers (Foundational & Advanced)

| Power_ID | Tier | Type | Forensic Effect | Optimization |
| :--- | :--- | :--- | :--- | :--- |
| **LUCK_FAR_REALM**| 1 | REAC | Force any hit to become a Critical Hit (1/LR).| **GOD (Crit)** |
| **FAV_BEGIN** | 1 | PASS | Add Proficiency Bonus to your first roll vs target.| **S (Init)** |
| **SHIELD_THRALL** | 1 | ACT | 10 Temp HP. If broken, potentially Stuns. | **A (Sustain)** |
| **TRANS_BREADTH** | 1 | MOVE | Teleport (18m). | **A (Move)** |
| **FORCE_TUNNEL** | 1 | ACT | Charge forward; Push targets 4m back. | **B (Area)** |
| **CONC_BLAST** | 1 | ACT | 3d6+Mod Psychic; Target must be Conc. | **B (Anti-Mag)**|
| **PSIONIC_OVERLD**| 1 | ACT | +1d4 Psychic dmg on hit (10t); Self dmg 1d4. | **B (DPR)** |
| **PERIL_STAKES** | 1 | ACT | Vulnerable to all dmg; Heal 2d8 per hit. | **A (Utility)** |
| **ABILITY_DRAIN** | 1 | PASS | Reduce target stat by 1 on hit (1/turn). | **S (Control)** |
| **STAGE_FRIGHT** | 1 | ACT | Disadv on attacks; Psychic dmg on miss. | **A (Control)** |
| **CHARM** | 1 | REAC | Prevent attacker from hitting you again (1t). | **A (Def)** |
| **CULL_THE_WEAK** | 2 | PASS | Auto-kill enemy if HP < (Unlocked Powers). | **S (Execute)** |
| **PSIONIC_BACK** | 2 | REAC | 1d4 Psychic dmg per spell lvl to caster. | **A (Anti-Mag)**|
| **DRAIN_STAT** | 2 | ACT | Drain attribute at low HP (1/LR). | **B (Utility)** |
| **REPULSOR** | 2 | ACT | 2d6 Force AoE; Push 6m. | **A (Area)** |
| **BLAST_LIMIT** | 2 | ACT | Stun multiple targets in cone. | **A (CC)** |
| **ABS_FORCE** | 2 | REAC | 1d4 Thunder dmg + Push 6m when hit. | **B (Def)** |

---

## ☢️ Matrix B: Tier 3 Supreme Powers (Partial Ceremorphosis)

| Power_ID | Tier | Type | Forensic Effect | Optimization |
| :--- | :--- | :--- | :--- | :--- |
| **FLY_TRAIT** | 3 | MOVE | Fly (18m). Permanent OA Immunity. | **GOD (Move)** |
| **MIND_SANCTU** | 3 | ZONE | Action and Bonus Action interchangeable. | **S (Action)** |
| **FREECAST** | 3 | REAC | Use Spell Slot/Charge for 0 cost (1/LR). | **S (Resource)**|
| **BLACK_HOLE** | 3 | ACT | Pull 5 targets to center; Slow (3m AoE). | **S (Control)** |
| **MIND_BLAST** | 3 | ACT | 4d8+Mod Psychic Conal; Stun 1 turn. | **S (CC)** |
| **FRACT_PSYCHE** | 3 | ACT | -1 AC to target per hit for 10 turns. | **A (Debuff)** |
| **ILLITHID_EXP** | 3 | ACT | Deal 10d10 force damage to target. | **A (Burst)** |
| **CONC_OVERL** | 3 | PASS | Damage adds Stun to concentration loss. | **A (CC)** |
| **ABS_PROTECT** | 3 | REAC | Grant target immunity to damage for 1 turn. | **A (Support)** |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "ILLITHID_V13.2",
  "manifest_ref": "vanguard_manifest.json#ILLITHID",
  "power_count": 26,
  "mechanics": {
    "cull_the_weak_calc": "SUM(unlocked_powers)",
    "mind_sanctuary_logic": "ACTION_BA_CONVERSION_ENABLED",
    "fly_bonus_action": false
  },
  "subsystems": {
    "STAT_DRAIN": ["STR", "DEX", "CON", "INT", "WIS", "CHA"],
    "REACTION_TRIGGERS": ["PSIONIC_BACKLASH", "CHARM", "ABSORB_FORCE", "LUCK_OF_THE_FAR_REALMS"]
  }
}
```
