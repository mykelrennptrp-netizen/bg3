---
id: CLASS_CLERIC
name: Cleric
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Cleric
primary_stat: WIS
secondary_stat: CON
tertiary_stat: [STR, DEX]
hp_base: 8
hp_scaling: 5
armor_prof: [LIGHT, MEDIUM, SHIELDS]
weapon_prof: [SIMPLE]
saving_throws: [WIS, CHA]
---

# ⛪ Cleric: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate strategy engine. It has been forensically satiated with the Octa-Matrix Standard, including **Step 1: The Core & Origin Domains**.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Cleric Rules
> - **Potent Spellcasting (P8)**: Corrected to add WIS modifier damage to necrotic cantrips (Toll the Dead).
> - **Storm's Fury (Tempest P8)**: Deals **LIGHTNING** damage (Reaction).
> - **Divine Intervention**: One-time-use per character (Lv 10+).

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | DOMAIN_SELECT | SELECT | - | Select Domain (Determines Armor/Spells). |
| **2** | CHANNEL_DIV | RESOURCE | 1_CHARGE | Use to Turn Undead or Domain Feature. |
| **5** | DESTROY_UNDEAD | PASSIVE | - | Turned Undead take **4d6 Radiant** if low level. |
| **6** | CHANNEL_DIV_2 | PASSIVE | - | Gain 2nd Channel Divinity Charge. |
| **8** | DIVINE_DOMAIN | SELECT | - | Gain Divine Strike or Potent Spellcasting. |
| **10** | DIV_INTERVENT | ACTION | 1_CHAR | Ultimate Prayer (One-time use). |

---

## Matrix B: Domain Hub (Optimization Biases)

| Subclass_ID | Role | Prof_Bonus | CD_Action | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **LIFE** | Pure Healer | Heavy Armor | Preserve Life | **S_TIER (Survival)** |
| **LIGHT** | Blaster / Offense| Med Armor | Radiance of Dawn | **GOD_TIER (Damage)** |
| **TEMPEST** | Lightning Nuke | Heavy/Martial| Destructive Wrath| **GOD_TIER (Burst)** |
| **WAR** | Frontline Gish | Heavy/Martial| Guided Strike | **A_TIER (Martial)** |
| **DEATH (P8)**| Necrotic Nuke | Martial | Touch of Death | **S_TIER (Necromancy)**|
| **KNOWLEDGE** | Skill Master | Med Armor | Knowledge of Ages| **A_TIER (Utility)** |
| **NATURE** | Elemental Tank | Heavy/Martial| Charm Animals | **B_TIER (Defense)** |
| **TRICKERY** | Stealth / Deco | Med Armor | Invoke Duplicity | **C_TIER (Strategy)** |

---

## Matrix C: Scaling Registry (Channel & Undead)

| Level | CD_Charges | Destroy_Undead_CR | Prof_Bonus | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **1** | 0 | - | +2 | [Wiki](https://bg3.wiki/wiki/Cleric) |
| **2** | 1 | - | +2 | [Wiki](https://bg3.wiki/wiki/Cleric) |
| **5** | 1 | CR 1/2 (4d6) | +3 | [Wiki](https://bg3.wiki/wiki/Cleric) |
| **6** | 2 | CR 1/2 (4d6) | +3 | [Wiki](https://bg3.wiki/wiki/Cleric) |
| **8** | 2 | CR 1 (4d6) | +3 | [Wiki](https://bg3.wiki/wiki/Cleric) |
| **11** | 2 | CR 2 (4d6) | +4 | [Wiki](https://bg3.wiki/wiki/Cleric) |

---

## Matrix G: Subclass Progression Registry (Granular - Batch 1)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **LIFE** | 1 | **LIFE_PROF** | PASSIVE | Gain Heavy Armor proficiency. |
| **LIFE** | 1 | **DISCIPLE_LIFE** | PASSIVE | Healing spells + [2 + Spell Lvl] HP. |
| **LIFE** | 2 | **PRESERVE_LIFE** | CD | AOE Heal [3 * Level] to all nearby allies. |
| **LIFE** | 6 | **BLESSED_HEAL** | PASSIVE | Heal self [2 + Spell Lvl] when healing others. |
| **LIFE** | 8 | **DIVINE_STRIKE** | PASSIVE | +1d8 Radiant on weapon hits. |
| **LIGHT** | 1 | **WARDING_FLARE** | REACT | Impose Disadv on attackers. |
| **LIGHT** | 1 | **LIGHT_CANTRIP** | CANTRIP | Gain Light cantrip automatically. |
| **LIGHT** | 2 | **RAD_OF_DAWN** | CD | 2d10+Level Radiant AOE. |
| **LIGHT** | 6 | **IMP_WAR_FLARE** | PASSIVE | Can use Warding Flare for allies. |
| **LIGHT** | 8 | **POTENT_CAST** | PASSIVE | Add WIS mod to cantrip damage. |
| **TEMPEST** | 1 | **TEMP_PROF** | PASSIVE | Gain Martial Weapon & Heavy Armor prof. |
| **TEMPEST** | 1 | **WRATH_STORM** | REACT | 2d8 Lightning/Thunder as reaction. |
| **TEMPEST** | 2 | **DEST_WRATH** | CD | Maximize Lightning/Thunder damage rolls. |
| **TEMPEST** | 6 | **THUNDERB_STRK** | PASSIVE | Push back targets [3m] with lightning dmg. |
| **TEMPEST** | 8 | **DIVINE_STRIKE** | PASSIVE | +1d8 Thunder on weapon hits. |
| **WAR** | 1 | **WAR_PROF** | PASSIVE | Gain Martial Weapon & Heavy Armor prof. |
| **WAR** | 1 | **WAR_PRIEST** | BONUS | Extra weapon attack using War Charges. |
| **WAR** | 2 | **GUIDED_STRIKE** | CD | +10 to Attack Rolls. |
| **WAR** | 6 | **WARGOD_BLESS** | REACT | +10 to an ALLY attack roll. |
| **WAR** | 8 | **DIVINE_STRIKE** | PASSIVE | +1d8 Weapon damage type on hits. |
| **DEATH (P8)**| 1 | **REAPER** | PASSIVE | Necromancy cantrips target 2 creatures (within 1.5m). |
| **DEATH (P8)**| 1 | **DEATH_PROF** | PASSIVE | Gain Martial Weapon proficiency. |
| **DEATH (P8)**| 2 | **TOUCH_DEATH** | CD | Add [5 + 2*Level] Necrotic damage on melee hit. |
| **DEATH (P8)**| 6 | **INESCAPABLE** | PASSIVE | Necrotic damage ignores Resistance. |
| **DEATH (P8)**| 8 | **DIVINE_STRIKE** | PASSIVE | +1d8 Necrotic damage on weapon hits. |
| **DEATH (P8)**| 10| **IMP_REAPER** | PASSIVE | Lv 1-5 Necromancy spells target 2 creatures. |
| **KNOWLEDGE** | 1 | **BLESS_KNOW** | PASSIVE | Expertise in 2: Arcana, History, Nature, Religion. |
| **KNOWLEDGE** | 2 | **KNOW_AGES** | CD | Proficiency in all skills of an Ability (Until rest). |
| **KNOWLEDGE** | 6 | **READ_THOUGHTS**| CD | Read thoughts of a creature while talking. |
| **KNOWLEDGE** | 8 | **POTENT_CAST** | PASSIVE | Add WIS mod to cantrip damage. |
| **NATURE** | 1 | **NATURE_PROF** | PASSIVE | Gain Heavy Armor proficiency. |
| **NATURE** | 1 | **NATURE_INIT** | CHOICE | Gain 1 Druid Cantrip & Animal/Nature skill. |
| **NATURE** | 2 | **CHARM_ANIM** | CD | Charm all nearby animals and plants. |
| **NATURE** | 6 | **DAMPEN_ELEM** | REACT | Halve damage of Acid, Cold, Fire, Light, Thunder. |
| **NATURE** | 8 | **DIVINE_STRIKE** | PASSIVE | +1d8 Cold, Fire, or Lightning on weapon hits. |
| **TRICKERY** | 1 | **BLESS_TRICK** | ACTION | Give ally Adv on Stealth checks. |
| **TRICKERY** | 2 | **INVOKE_DUP** | CD | Create illusion for Adv on attacks nearby. |
| **TRICKERY** | 6 | **CLOAK_SHADOW**| CD | Become Invisible until attacking/casting. |
| **TRICKERY** | 8 | **DIVINE_STRIKE** | PASSIVE | +1d8 Poison damage on weapon hits. |

---

## Matrix E: Domain Spell Matrix (Step 1)

| Domain | Lv 1 Spells | Lv 3 Spells | Lv 5 Spells | Lv 7 Spells | Lv 9 Spells |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **LIFE** | Bless, Cure Wounds | Aid, Lesser Restore | Revivify, Beacon | Death Ward, Guardian | Mass Cure, Raise Dead |
| **LIGHT** | Burning H, Faerie F | Flaming Sp, Scorcher | Fireball, Daylight | Wall Fire, Guardian | Destr Wave, Flame Strike |
| **TEMPEST** | Fog Cloud, Thunderw | Gust Wind, Shatter | Call Light, Sleet St | Ice Storm, Freedom M | Destr Wave, Insect Plagues|
| **WAR** | Div Favour, Shield F | Magic Weapon, Spirit G | Elem Weapon, Spirit G | Freedom Move, Stoneskin | Flame Strike, Hold Monstr|
| **DEATH (P8)**| False Life, Sick Ray| Blindness, Ray Enfeeble| Animate Dead, Vamp Touch| Blight, Death Ward | Antilife Shell, Cloudkill|
| **KNOWLEDGE** | Command, Sleep | Blindness, Calm Emot | Slow, Speak w/ Dead | Confusion, Otiluke Res | Dominate Pers, Telekin |
| **NATURE** | Animal Fr, Speak Anim| Barkskin, Spike Growth | Plant Growth, Sleet St | Dominate Beast, Grasp V | Insect Plague, Wall Stone|
| **TRICKERY** | Charm Pers, Disguise | Mirror Image, Pass Tr | Bestow Curse, Fear | Dimension Door, Polymorph| Dominate Person, Mod Mem |

---

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Radiant Orb Stacking**: Light Domain + Spirit Guardians + Luminous Armor is the premier AOE debuff strategy.
> - **Lightning Nuke**: Tempest Cleric max-damage CDs must be synchronized with `Witch Bolt` (Lv 6) or `Chain Lightning` for maximum single-target deletion.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "CLERIC_V13.2",
  "manifest_ref": "vanguard_manifest.json#CLERIC",
  "patch_baseline": "8_HOTFIX36",
  "building_priorities": {
    "stat_weight": {"WIS": 1.0, "CON": 0.8, "STR": 0.6, "DEX": 0.4},
    "multiclass_dips": {
      "Sorcerer_Tempest": "Destructive_Wrath_Combo",
      "Fighter_1": "Constitution_Saving_Throw_Start",
      "Wizard_Necro": "Undead_Army_Death_Synergy"
    },
    "feat_ranking": ["War_Caster", "Alert", "Resilient_CON", "Ability_Improvement"]
  },
  "subclass_logic": {
    "death_reaper_range": 1.5,
    "life_disciple_bonus": "2_PLUS_LVL",
    "tempest_push_logic": "THUNDERBOLT_3M",
    "knowledge_ages_reset": "LONG_REST"
  }
}
```


