---
id: LIBRARY_CONDITION_REGISTRY
name: Global Condition & Status Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Conditions
logic_type: STATUS_EFFECT_MAPPING
---

# ☣️ Conditions: v13.2 High-Fidelity Standard (Patch 8)

This node governs the status effects and debuffs that impact combat math. It has been forensically satiated with the Octa-Matrix Standard, including **Radiant Orb** and **Reverberation** synergy chains.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Condition Rules
> - **Stacking (SSoT)**: Most conditions (e.g., *Radiant Orb*, *Reverberation*) stack up to 7-10 times. 
> - **Incapacitated**: A character who is incapacitated (Stunned, Paralyzed, Sleeping) cannot take actions or reactions and automatically fails STR/DEX saves.
> - **Prone**: Attacking a prone target within 1.5m grants Advantage. Prone targets have Disadvantage on Strength and Dexterity saving throws.

---

## 📊 Matrix A: High-Impact CC & DOT Conditions

| Condition_ID | Type | Forensic Effect | Degradation | Optimization |
| :--- | :--- | :--- | :--- | :--- |
| **STUNNED** | CC | Cannot move/act/reac. | 1 Turn | **GOD (Lock)** |
| **PARALYZED** | CC | Incapacitated; Auto-crit <1.5m. | 1 Turn | **GOD (DPR)** |
| **PRONE** | DEBUFF | Cannot move/act. Stand=50% Speed. | End of Turn | **S (Control)** |
| **RAD_ORB** | DEBUFF | -1 to Attack Rolls per stack. | -2 Stacks | **S (Defense)** |
| **REVERB** | DEBUFF | -1 to STR/DEX/CON saves per stack. | -1 Stack | **S (Synergy)** |
| **ARCANE_ACU** | BUFF | +1 to Spell Attack/Save DC per stack.| -2 Stacks | **GOD (Caster)** |
| **MENT_FATIG** | DEBUFF | -1 to INT/WIS/CHA saves per stack. | -1 Stack | **S (Control)** |
| **WET** | DEBUFF | Vuln Cold/Light; Resist Fire. | 3 Turns | **S (Combo)** |
| **BANE** | DEBUFF | -1d4 to Attack Rolls and Saving Throws. | 10 Turns | **S (Debuff)** |
| **FAERIE_FIRE**| DEBUFF | Advantage on all attack rolls. | 10 Turns | **S (Reliability)**|
| **FRIGHTENED** | CC | No move to source; Disadv. | 2 Turns | **A (Control)** |
| **SILENCED** | CC | Cannot cast Verbal spells. | 10 Turns | **A (Anti-Mage)**|
| **POISONED** | DEBUFF | Disadv on Attack/Ability Checks. | 1-3 Turns | **A (Debuff)** |
| **ENSNARED** | CC | No move; Disadv Attack/DEX saves. | 10 Turns | **B (Control)** |
| **RESTRAINED** | CC | No move; Disadv Attack/DEX saves. | 10 Turns | **B (Control)** |
| **BLEEDING** | DOT | 2 Slashing dmg; Disadv CON saves. | 1-3 Turns | **B (DOT)** |
| **BURNING** | DOT | 1d4 Fire dmg/turn. | 1-3 Turns | **C (DOT)** |
| **HEAT** | BUFF | Consume for extra Fire dmg. | -1 Stack | **C (Niche)** |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "COND_REGISTRY_V13.2",
  "manifest_ref": "vanguard_manifest.json#CONDITIONS",
  "patch_baseline": "8_HOTFIX36",
  "condition_logic": {
    "PARALYZED": {"auto_crit_range": 1.5, "incapacitated": true},
    "WET": {"vulnerability": ["COLD", "LIGHTNING"], "resistance": ["FIRE"]},
    "RADIANT_ORB": {"attack_penalty_per_stack": 1, "max_stacks": 10},
    "REVERBERATION": {"save_penalty_per_stack": 1, "trigger_threshold": 5, "trigger_dmg": "1d4_Thunder"}
  },
  "synergy_mapping": {
    "WET_BOLT": ["CREATE_WATER", "CHAIN_LIGHTNING"],
    "ORB_BUILD": ["LUMINOUS_ARMOUR", "SPIRIT_GUARDIANS"]
  }
}
```
