---
id: CLASS_BARBARIAN
name: Barbarian
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Barbarian
primary_stat: STR
secondary_stat: CON
tertiary_stat: DEX
hp_base: 12
hp_scaling: 7
armor_prof: [LIGHT, MEDIUM, SHIELDS]
weapon_prof: [SIMPLE, MARTIAL]
saving_throws: [STR, CON]
---

# 🪓 Barbarian: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate frontline agent. It has been forensically satiated with granular level-progression data (Matrix G) and automated optimization biases.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Barbarian Rules
> - **Rage (SSoT)**: +2 damage (Lv 1-8), +3 (Lv 9-12). Resistance to Physical damage.
> - **Wildheart Off-hand (P8)**: Fixed bug where STR mod was being added twice; now correctly adds **Bonus Damage** to off-hand melee weapon attacks.
> - **Rage Scaling (P8)**: Wildheart rages now correctly deal improved damage past **Level 9**.
> - **Tiger's Bloodlust (P8)**: Bleed damage scaling and cleave target logic verified (Targets 3).
- **Giant (P8)**: 
    - **Giant's Power**: Become Large; +d4/d6 damage.
    - **Mighty Impel**: Throw enemies/allies as a Bonus Action.

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | RAGE | BONUS | 1_CHARGE | Gain Resistances, Damage bonus, STR Adv. |
| **1** | UNARMORED_DEF | PASSIVE | - | AC = 10 + DEX + CON. |
| **2** | RECKLESS_ATT | ACTION | - | Advantage on Melee; Enemies Adv on you. |
| **2** | DANGER_SENSE | PASSIVE | - | Adv on DEX saves vs traps/spells. |
| **5** | EXTRA_ATTACK | PASSIVE | - | Attack twice per Action. |
| **5** | FAST_MOVEMENT | PASSIVE | - | +3m Speed when not in Heavy Armor. |
| **7** | FERAL_INSTINCT | PASSIVE | - | +3 Initiative; Can't be Surprised. |
| **9** | BRUTAL_CRIT | PASSIVE | - | Gain extra damage die on Critical Hits. |
| **11** | RELENT_RAGE | PASSIVE | - | Drop to 1 HP instead of 0 (Once per rest). |

---

## Matrix B: Subclass Hub (Building Biases)

| Subclass_ID | Theme | Strength | Playstyle | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **BERSERKER** | Pure Fury | Single-Target DPR | Aggressive | **GOD_TIER (Throwing)** |
| **WILD_HEART**| Primal Bond | Tanking/Utility | Tactical | **S_TIER (Bear/Tiger)** |
| **WILD_MAGIC**| Arcane Surge | Support/Chaos | Adaptive | **A_TIER (Utility)** |
| **GIANT (P8)** | Colossal Power | Battlefield Control| Utility | **GOD_TIER (Controls)** |

---

## Matrix C: Scaling Registry (Rage & Math)

| Level | Rage_Charges | Rage_Damage | Prof_Bonus | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **1** | 2 | +2 | +2 | [Wiki](https://bg3.wiki/wiki/Barbarian) |
| **3** | 3 | +2 | +2 | [Wiki](https://bg3.wiki/wiki/Barbarian) |
| **6** | 4 | +2 | +3 | [Wiki](https://bg3.wiki/wiki/Barbarian) |
| **9** | 4 | +3 | +4 | [Wiki](https://bg3.wiki/wiki/Barbarian) |
| **12**| 5 | +3 | +4 | [Wiki](https://bg3.wiki/wiki/Barbarian) |

---

## Matrix G: Subclass Progression Registry (Granular)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **BERSERKER** | 3 | **FRENZY** | BONUS | Rage upgrade; enables Bonus Action attacks. |
| **BERSERKER** | 3 | **FRENZIED_STRIKE**| BONUS | Melee attack as a Bonus Action. |
| **BERSERKER** | 3 | **ENRAGED_THROW** | BONUS | Throw creature/object; Inflicts Prone. |
| **BERSERKER** | 6 | **MINDLESS_RAGE** | PASSIVE | Immune to Charmed/Frightened while Frenzied. |
| **BERSERKER** | 10| **INTIM_PRESENCE** | ACTION | Satiate target with Fear (Uses CHA). |
| **WILD_HEART**| 3 | **BESTIAL_HEART** | CHOICE | Select Bear, Eagle, Elk, Tiger, or Wolf. |
| **WILD_HEART**| 3 | **TALK_ANIMALS** | SPELL | Permanent ritual spell access. |
| **WILD_HEART**| 6 | **ANIMAL_ASPECT** | CHOICE | Selection Pool E (Passive traits). |
| **WILD_HEART**| 8 | **LANDS_STRIDE** | PASSIVE | Ignore Difficult Terrain. |
| **WILD_HEART**| 10| **ADD_ASPECT** | CHOICE | Select secondary Animal Aspect. |
| **WILD_MAGIC**| 3 | **MAG_AWARENESS** | ACTION | Reveal location of spells to allies (Prof Range).|
| **WILD_MAGIC**| 3 | **WILD_SURGE** | TRIGGER | 100% chance to surge when Raging. |
| **WILD_MAGIC**| 6 | **BOLSTER_BOON** | ACTION | +1d4 to Attack Rolls & Ability Checks. |
| **WILD_MAGIC**| 6 | **RESTORE_L1_L2** | ACTION | Restore Level 1 or 2 spell slot to ally. |
| **WILD_MAGIC**| 9 | **RESTORE_L3** | ACTION | Restore Level 3 spell slot to ally. |
| **WILD_MAGIC**| 10| **UNSTABLE_BACK** | REACT | Surge again when taking damage/failing save. |
| **GIANT (P8)** | 3 | **GIANTS_RAGE** | PASSIVE | Become Large; +d4 damage; Reach increased. |
| **GIANT (P8)** | 3 | **VAPRAK_GREED** | PASSIVE | Adv on STR checks; Carry weight doubled. |
| **GIANT (P8)** | 3 | **THAUMATURGY** | CANTRIP | +Adv on Intimidation/Performance. |
| **GIANT (P8)** | 5 | **BOOT_OF_GIANTS** | PASSIVE | Athletics +1; Jump distance scaling. |
| **GIANT (P8)** | 6 | **ELEM_CLEAVER** | ACTION | Infuse weapon w/ 1d6 Elemental; Returning. |
| **GIANT (P8)** | 10| **MIGHTY_IMPEL** | BONUS | Throw creature (even Large) as Bonus Action. |

---

## Matrix D: Synergy DNA (Agent-Reasoning Tags)

| Tag_ID | Optimization_Trigger | Satiation_Status | Logic_Anchor |
| :--- | :--- | :--- | :--- |
| **THROW_GOD** | Berserker/Giant + Tavern Brawler. | **SATIATED** | [Matrix F](#matrix-f-build-synergy-biases-agent-logic) |
| **RESIST_TANK** | Bear Heart + Heavy Armor (Dip). | **SATIATED** | [Matrix F](#matrix-f-build-synergy-biases-agent-logic) |
| **MAIM_LOCK** | Tiger Heart + Wolverine Aspect. | **SATIATED** | [Matrix F](#matrix-f-build-synergy-biases-agent-logic) |
| **CRIT_STUNT** | Champion Dip + Reckless Attack. | **SATIATED** | [Matrix F](#matrix-f-build-synergy-biases-agent-logic) |

---

## Matrix E: Selection Pool Matrix (Full Forensic Pools)

| Pool_ID | Choice_ID | Type | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- | :--- |
| **HEART** | Bear | Rage | **S** | Resistance to ALL damage (except Psychic). |
| **HEART** | Tiger | Rage | **S** | Tiger's Bloodlust (Cleave/Bleed logic). |
| **HEART** | Eagle | Rage | **A** | Diving Strike; Disadv on enemy OA; Dash as BA. |
| **HEART** | Elk | Rage | **B** | Stampede (Prone) + Increased movement speed. |
| **HEART** | Wolf | Rage | **B** | Incite Fury (Advantage for all melee allies). |
| **ASPECT**| Wolverine | Aspect | **S** | Maim targets if Bleeding (Tiger Combo). |
| **ASPECT**| Bear | Aspect | **S** | Double Carry Capacity + STR check Advantage. |
| **ASPECT**| Tiger | Aspect | **A** | Add STR mod to Attack vs Bleeding/Poisoned. |
| **ASPECT**| Stallion | Aspect | **A** | Temp HP [2 * Lvl] on Dash (Massive Sustain). |
| **ASPECT**| Chimpanzee | Aspect | **B** | Throwing camp supplies blinds targets. |
| **ASPECT**| Crocodile | Aspect | **B** | 3m Speed bonus on Water, Grease, Mud. |
| **ASPECT**| Eagle | Aspect | **B** | Darkvision 12m + Perception check Adv. |
| **ASPECT**| Elk | Aspect | **B** | Critical for allies speed within 18m. |
| **ASPECT**| Honey Badger| Aspect | **B** | 50% chance to Rage on poisoned/charmed/fear. |
| **ASPECT**| Wolf | Aspect | **C** | Stealth & Sleight of Hand check Adv. |

---

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Thrower Bias**: Berserker/Giant + Tavern Brawler is the highest DPR baseline. Prioritize `STR` elixirs to free up feat slots for `Alert`.
> - **Maim-Lock**: Tiger Heart + Wolverine Aspect effectively removes target threat by reducing speed to 0.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "BARBARIAN_V13.2",
  "manifest_ref": "vanguard_manifest.json#BARBARIAN",
  "patch_baseline": "8_HOTFIX36",
  "building_priorities": {
    "stat_weight": {"STR": 1.0, "CON": 0.8, "DEX": 0.6},
    "multiclass_dips": {
      "Fighter_2": "Action_Surge",
      "Rogue_Thief": "Additional_Bonus_Action"
    },
    "feat_ranking": ["GWM", "Tavern_Brawler", "Alert", "Sentinel"]
  },
  "subclass_logic": {
    "giant_p8_reach_bonus": 1.5,
    "wild_magic_restore_priority": "MAX_SLOT",
    "berserker_frenzy_penalty": "STACKING_ATTACK_MALUS"
  }
}
```



