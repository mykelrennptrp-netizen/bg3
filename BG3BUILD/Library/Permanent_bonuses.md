---
id: LIBRARY_PERMANENT_BONUSES
name: Permanent Boons & Scaling Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Permanent_bonuses
logic_type: ATTRIBUTE_CAP_EXTENSION
---

# 🏆 Permanent Bonuses: v13.2 High-Fidelity Standard (Patch 8)

This node governs the unique permanent overrides that allow builds to exceed standard attribute caps. It has been forensically satiated with the Octa-Matrix Standard for Gemini Pro optimization.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Bonus Rules
> - **Attribute Caps**: Ethel's Hair and Mirror of Loss are the ONLY ways to reach Attribute Score **24** (combined with specific gear).
> - **Acquisition Lock**: These are permanent once applied and cannot be respecced or transferred via Withers.
> - **The Mirror Check**: Using the Mirror of Loss requires passing a series of high DC checks (Religion and Arcana).

---

## 📊 Matrix A: Primary Attribute Augments (The "Big Three")

| Boon_ID | Source | Act | Mechanical Effect_Forensic | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **ETHEL_HAIR** | Auntie Ethel | 1 | +1 to any chosen Attribute. | **GOD_TIER (Stat-Patch)** |
| **MIRROR_LOSS**| Mirror / House | 3 | +2 to any chosen Attribute. (Max 24). | **GOD_TIER (Stat-Cap)** |
| **VIGOUR_POT** | Araj Oblodra | 2 | +2 to Strength (Permanent). | **S_TIER (STR Martials)** |
| **THAN_NECRO** | Thay Tome | 1/3 | Speak with Dead + 20 Temp HP on Long Rest. | **S_TIER (Sustain)** |

---

## ⚡ Matrix B: Strategic Secondary Boons

| Boon_ID | Type | Effect | Acquisition Condition |
| :--- | :--- | :--- | :--- |
| **GITH_BARRIER**| PASSIVE | Advantage on INT Saving Throws. | Steal Githzerai Mind Barrier (Act 2). |
| **ABS_BRAND** | PASSIVE | Enables "Absolute" gear properties. | Branded by Gut (Act 1). |
| **LOVIATAR_L** | PASSIVE | +2 Attack/Save when below 30% HP. | Abdirak's Penance (Act 1). |
| **VOLO_EYE** | PASSIVE | Permanent See Invisibility (3m). | Volo's Surgery (Act 1). |
| **BOAL_BENE** | PASSIVE | Advantage on Attacks vs Bleeding targets. | Sacrifice ally to BOAL (Act 1). |
| **VAMP_ASCEN** | PASSIVE | +1d10 Necrotic to hits; Misty Escape (Reac).| Astarion Ritual (Act 3). |
| **SLAYER_FORM**| PASSIVE | Access to Slayer Transformation (High HP). | Dark Urge Event (Act 2/3). |
| **PIXIE_BLESS** | PASSIVE | Immune to Shadow Curse (Light/Heavy). | Release Pixie from Lantern (Act 2). |
| **ARABELLA_E** | SPELL | Free cast of Arabella's Entangle. | Complete Arabella's quest (Act 2). |
| **SURVIV_INST** | REAC | Target heals if it drops to 0 HP. | Omeluum's experimental potion (Act 1).|
| **ALFIRA_INS** | PASSIVE | +1d6 to all Ability Checks. | Help Alfira write her song (Act 1). |
| **WAKING_MIND** | PASSIVE | Advantage on all Proficiency checks. | Consume Waking Mind (Act 2). |
| **AWAKENED** | PASSIVE | Illithid Powers cost Bonus Action. | Pass Zaith'isk saving throws (Act 1). |
| **MONK_CURSE** | SPELL | Tasha's Laughter effect on hit. | Help Sentient Amulet (Act 1/3). |
| **SWEET_STIG** | PASSIVE | Resistance to RAD damage. | Complete 'Investigate Murders' (Act 3).|

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "PERMANENT_BONUSES_V13.2",
  "manifest_ref": "vanguard_manifest.json#BONUSES",
  "patch_baseline": "8_HOTFIX36",
  "scaling_formulas": {
    "mirror_of_loss": "+2_ANY",
    "ethel_hair": "+1_ANY",
    "everlasting_vigour": "+2_STR",
    "attribute_cap_ceiling": 24
  },
  "synergy_mapping": {
    "ACTOR_HALF_FEAT": ["ETHEL_HAIR_CHA", "ACTOR_FEAT", "Score_18_Lv1"],
    "STR_CEILING": ["CLOUD_GIANT_ELIXIR", "VIGOUR_POTION", "MIRROR_STR"]
  }
}
```
