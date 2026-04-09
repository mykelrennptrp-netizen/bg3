---
id: CLASS_BARD
name: Bard
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Bard
primary_stat: CHA
secondary_stat: DEX
tertiary_stat: CON
hp_base: 8
hp_scaling: 5
armor_prof: [LIGHT]
weapon_prof: [HAND_XBOW, LONG_SWORD, RAPIER, SHORT_SWORD, SIMPLE]
saving_throws: [DEX, CHA]
---

# 🎻 Bard: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate versatile agent. It has been forensically satiated with the Octa-Matrix Standard, including the primary Patch 8 additive: **College of Glamour**.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Bard Rules
> - **Bardic Inspiration (SSoT)**: Bonus Action buff. Recovers on **Short Rest** at Lv 5+. Scales: d6 -> d8 -> d10.
> - **Jack of All Trades**: Add half proficiency (rounded down) to all non-proficient skill checks.
> - **Magical Secrets**: Learn spells from any class. Lore (Lv 6 & 10), Others (Lv 10 only).
> - **Song of Rest**: Grants the benefit of a Short Rest (Once per Long Rest).

---

---

## 📊 Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | BARDIC_INSP | BONUS | 1_CHARGE | Buff ally Attack, Save, or Ability check. |
| **2** | JACK_TRADES | PASSIVE | - | Add 0.5x Prof to untrained skills. |
| **2** | SONG_OF_REST | ACTION | 1_PER_LR | Extra Short Rest utility for the party. |
| **3** | EXPERTISE | SELECT | - | Double Proficiency in 2 chosen skills. |
| **5** | FONT_OF_INSP | PASSIVE | - | Inspiration now recovers on **SHORT REST**. |
| **6** | COUNTERCHARM | ACTION | - | Adv on saves vs Charmed/Frightened (7m). |
| **10** | MAGICAL_SECR | SELECT | - | Learn 2 spells from ANY class list. |
| **10** | EXPERTISE_2 | SELECT | - | Double Proficiency in 2 additional skills. |

---

---

## 🎨 Matrix B: College Hub (Building Biases)

| Subclass_ID | Theme | Strength | Playstyle | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **LORE** | Forbidden Knowledge | Controlling/Magic | Caster | **GOD_TIER (Magic)** |
| **SWORDS** | Flourishing Blade | Melee/Ranged DPR | Gish/Striker | **GOD_TIER (Martial)**|
| **GLAMOUR (P8)**| Fae Majesty | Tactical Control | Buffer/Controller| **S_TIER (Utility)** |
| **SPIRITS (P8)**| Spirit Medium | Tales/Buffs | Random Utility | **A_TIER (Adaptive)**|
| **VALOUR** | Combat Valor | Frontline Support | Defensive Gish| **A_TIER (Hybrid)** |

---

---

## 📈 Matrix C: Scaling Registry (Inspiration & Slots)

| Level | Inspiration_Die | Recovery | Prof_Bonus | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **1** | 1d6 | Long Rest | +2 | [Wiki](https://bg3.wiki/wiki/Bard) |
| **5** | 1d8 | Short Rest | +3 | [Wiki](https://bg3.wiki/wiki/Bard) |
| **9** | 1d8 | Short Rest | +4 | [Wiki](https://bg3.wiki/wiki/Bard) |
| **10** | 1d10 | Short Rest | +4 | [Wiki](https://bg3.wiki/wiki/Bard) |

---

## Matrix G: Subclass Progression Registry (Granular)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **LORE** | 3 | **CUTTING_WORDS** | REACT | Subtract 1d6/8/10 from enemy rolls. |
| **LORE** | 3 | **BONUS_PROF** | PASSIVE | Gain Arcana, Intimidation, Sleight of Hand. |
| **LORE** | 6 | **ADD_MAG_SECR** | SELECT | Learn 2 additional spells from any class. |
| **SWORDS** | 3 | **SWORD_PROF** | PASSIVE | Gain Med Armor and Scimitar proficiency. |
| **SWORDS** | 3 | **FIGHT_STYLE** | CHOICE | Select Duelling or Two-Weapon Fighting. |
| **SWORDS** | 3 | **FLOURISHES** | ACTION | Slashing (2 Tar), Defensive, and Mobile (Tele-on-kill P8). |
| **SWORDS** | 6 | **EXTRA_ATTACK** | PASSIVE | Attack twice per Action. |
| **GLAMOUR (P8)**| 3 | **MANTLE_INSP** | BONUS | Allies gain Temp HP + Move as a Reaction. |
| **GLAMOUR (P8)**| 3 | **ENTHRALL_PERF** | ACTION | Charm targets for 1 minute (Social utility). |
| **GLAMOUR (P8)**| 6 | **MANTLE_MAJ** | BONUS | Cast **COMMAND** every turn for 10 turns (P8).|
| **SPIRITS (P8)**| 3 | **SPIRIT_TALES** | SELECT | Use Inspiration to roll for Spirit buffs. |
| **SPIRITS (P8)**| 3 | **GUID_WHISPER** | CANTRIP | Gain **Guidance** (60ft range). |
| **SPIRITS (P8)**| 6 | **SPIRIT_SESS** | ACTION | Channel spirits to learn a temporary spell. |
| **VALOUR** | 3 | **VALOUR_PROF** | PASSIVE | Gain Med Armor, Shields, Martial Weapons. |
| **VALOUR** | 3 | **COMBAT_INSP** | BONUS | Insp applies to Damage or Armour Class. |
| **VALOUR** | 6 | **EXTRA_ATTACK** | PASSIVE | Attack twice per Action. |

---

## Matrix E: Selection Pool Matrix (Full Forensic Pools)

| Pool_ID | Choice_ID | Access_Lvl | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- | :--- |
| **MAG_SECR** | **COUNTERSPELL** | 6 (Lore) | **S** | Mandatory for action economy denial. |
| **MAG_SECR** | **HUNGER_HADAR**| 6 (Lore) | **S** | Premier Level 3 control/damage zone. |
| **MAG_SECR** | **HASTE** | 6 (Lore) | **S** | Best multiplier for Swords/Valour/Allies. |
| **MAG_SECR** | **BANISH_SMITE**| 10 (All) | **S** | 5d10 Force + Banishment (Swords Gish King).|
| **MAG_SECR** | **ARMOR_AGATHYS**| 6 (Lore) | **A** | Massive Temp HP + Reflect dmg for frontliners.|
| **MAG_SECR** | **SPIRIT_GUARD**| 6 (Lore) | **A** | Continuous AOE Radiant/Necro; Frontline god.|
| **MAG_SECR** | **SLOW** | 6 (Lore) | **A** | Massive multi-target debuff; Denies actions. |
| **MAG_SECR** | **CONJ_ELEMENT**| 10 (All) | **A** | Summons Myrmidons/Elementals (Action soak). |
| **MAG_SECR** | **SANCTUARY** | 6 (Lore) | **A** | Powerful BA defense for squishy allies. |
| **MAG_SECR** | **FIREBALL** | 6 (Lore) | **B** | Standard AOE blast if party lacks damage. |
| **MAG_SECR** | **HOLD_MONSTER**| 10 (All) | **B** | High-level control; Auto-crits for allies. |
| **MAG_SECR** | **CONE_COLD** | 10 (All) | **B** | Massive AOE damage + potential Freeze. |
| **MAG_SECR** | **MIRROR_IMAGE**| 6 (Lore) | **C** | Concentration-free AC boost. |
| **MAG_SECR** | **WARDEN_VIT** | 6 (Lore) | **C** | Sustained BA healing; Now castable with Level 4-6 slots (P8). |
| **EXPERTISE** | Persuasion | - | **S** | Mandatory for social-based social engine. |
| **EXPERTISE** | Perception | - | **S** | Critical for trap/hidden item detection. |
| **EXPERTISE** | Sleight Hand | - | **A** | Lockpicking/Pickpocketing dominance. |
| **EXPERTISE** | Arcana/History| - | **B** | Social/Lore check specialization. |

---

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Magical Secrets Focus**: Prioritize `Counterspell` and `Hunger of Hadar` for Lore Bards at Level 6 to seize action economy control early.
> - **Stat Bias**: Maintain `CHA 20` for maximum DC on control spells before investing in `DEX` initiative.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "BARD_V13.2",
  "manifest_ref": "vanguard_manifest.json#BARD",
  "patch_baseline": "8_HOTFIX36",
  "building_priorities": {
    "stat_weight": {"CHA": 1.0, "DEX": 0.8, "CON": 0.6},
    "multiclass_dips": {
      "Paladin_2": "Divine_Smite_Enable",
      "Warlock_2": "Eldritch_Blast_Fallback",
      "Wizard_1": "Spell_Scribing_Utility"
    },
    "feat_ranking": ["Alert", "Sharpshooter", "War_Caster", "Actor"]
  },
  "subclass_logic": {
    "glamour_mantle_reposition": "REACTION_BY_ALLY",
    "spirits_tales_inspir_cost": 1,
    "swords_flourish_action_cost": "ACTION_KNOT",
    "lore_cutting_words_trigger": "REACTION_ON_SUCCESS"
  }
}
```



