---
id: LOGIC_MULTICLASSING
name: Global Multiclassing Logic
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Multiclassing
logic_type: RELATIONAL_SYNERGY
optimization_dna: [DIP_OPTIMIZATION, SAD_BUILD, CASTER_SCALING]
---

# 🔀 Multiclassing Logic: v13.2 High-Fidelity Standard (Patch 8)

This node governs the interaction between different disciplines. In BG3, specific rounding and stacking exceptions differ from 5e tabletop.

## [WIKI_LOCK] Core Multiclassing Rules
- **Rounding (SSoT)**: Fractional spell slot contributions (Half/Third casters) are **rounded down PER CLASS** before summing.
- **Extra Attack Stacking**: High-Fidelity deviation.
    - **Standard/Tactician**: Pact of the Blade (Warlock 5) **STACKS** with Martial Extra Attack (Fighter/Paladin 5) for 3 attacks.
    - **Honour Mode**: These **DO NOT STACK**. Maximum 2 attacks per Action.
- **Proficiency**: Total Character Level (1-12) determines the bonus.

---

## Matrix A: Multiclass Entry Proficiencies

| Class_Entered | Armour_Gained | Weapon_Gained | Skill_Gained |
| :--- | :--- | :--- | :--- |
| **BARBARIAN** | Shields | - | - |
| **BARD** | Light | 1 Skill | - |
| **CLERIC** | Light, Medium, Shields | - | - |
| **DRUID** | Light, Medium, Shields | - | - |
| **FIGHTER** | Light, Medium, Shields | MARTIAL | - |
| **MONK** | - | - | - |
| **PALADIN** | Light, Medium, Shields | MARTIAL | - |
| **RANGER** | Light, Medium, Shields | MARTIAL + 1 Skill | - |
| **ROGUE** | Light | - | 1 Skill + Thieves' Tools |

> [!IMPORTANT]
> **HEAVY ARMOR LOCK**: Heavy Armor proficiency is only gained if the *First Class* provides it (Fighter/Paladin) OR if the multiclassed subclass provides it (Life/Tempest/War/Death Cleric).

---

## Matrix B: Spell Slot Caster Level Weighting

| Class_Type | Multiplier | Classes | wiki_Anchor |
| :--- | :--- | :--- | :--- |
| **FULL** | 1.0 | Bard, Cleric, Druid, Sorcerer, Wizard | [Wiki](https://bg3.wiki/wiki/Spells) |
| **HALF** | 0.5 | Paladin, Ranger (Rounded DOWN per class). | [Wiki](https://bg3.wiki/wiki/Spells) |
| **THIRD** | 0.33 | Arcane Trickster, Eldritch Knight (Down). | [Wiki](https://bg3.wiki/wiki/Spells) |

---

## Matrix C: Action Economy Stacking (Extra Attack)

| Interaction_ID | Mode: Standard/Tactician | Mode: Honour | wiki_Anchor |
| :--- | :--- | :--- | :--- |
| **Fighter 5 + Paladin 5** | 2 Attacks (No Stack) | 2 Attacks (No Stack)| [Wiki](https://bg3.wiki/wiki/Extra_Attack) |
| **Warlock 5 + Paladin 5** | **3 Attacks** (Stack!) | 2 Attacks (No Stack)| [Wiki](https://bg3.wiki/wiki/Extra_Attack) |
| **Monk 5 + Ranger 5** | 2 Attacks (No Stack) | 2 Attacks (No Stack)| [Wiki](https://bg3.wiki/wiki/Extra_Attack) |

---

## Matrix D: Synergy DNA (Agent-Optimization)

| Tag_ID | Optimization_Trigger | Satiation_Status |
| :--- | :--- | :--- |
| **DIP_FIGHTER_2** | Action Surge for any Caster/Striker. | **SATIATED** |
| **DIP_WARLOCK_1** | Hexblade SAD/Melee scaling (Patch 8). | **SATIATED** |
| **DIP_CLERIC_1** | Heavy Armor + Domain Passives. | **SATIATED** |
| **DIP_ROGUE_3** | Thief (Fast Hands) for dual-wielding. | **SATIATED** |

---

## Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "MULTICLASSING",
  "patch_baseline": "8_HOTFIX36",
  "caster_calc": {
    "Bard": 1.0, "Cleric": 1.0, "Druid": 1.0, "Sorcerer": 1.0, "Wizard": 1.0,
    "Paladin": 0.5, "Ranger": 0.5,
    "Arcane_Trickster": 0.33, "Eldritch_Knight": 0.33
  },
  "rounding": "FLOOR_PER_CLASS",
  "warlock_pact_stacking": {
    "standard": true,
    "tactician": true,
    "honour": false
  }
}
```


