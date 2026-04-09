---
id: CLASS_PALADIN
name: Paladin
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Paladin
primary_stat: STR
secondary_stat: CHA
tertiary_stat: CON
hp_base: 10
hp_scaling: 6
armor_prof: [LIGHT, MEDIUM, HEAVY, SHIELDS]
weapon_prof: [SIMPLE, MARTIAL]
saving_throws: [WIS, CHA]
---

# 🛡️ Paladin: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate holy warrior. It has been forensically satiated with the Octa-Matrix Standard, including **Step 1: Core & Primary Oaths**.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Paladin Rules
> - **Divine Smite (SSoT)**: Consumes spell slot to add 2d8 base (L1) + 1d8 per slot level. Max cap: **5d8**.
> - **Aura of Protection (Lv 6)**: Adds CHA Mod to all Saving Throws for self and allies within 3m. Unarmored Defense conflict handled.
> - **Improved Divine Smite (Lv 11)**: All melee attacks gain a permanent **1d8 Radiant** damage bonus.
> - **Vow of Enmity (Tactical)**: Casting Vow of Enmity on **self** grants Advantage on attack rolls against all enemies (10 turns).

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | OATH_SELECT | SELECT | - | Select Paladin Oath (Subclass). |
| **2** | DIVINE_SMITE | ACTION | 1_SLOT | Main burst; Can be used on hits via Reaction toggle. |
| **2** | FIGHT_STYLE | SELECT | - | Defense, Dueling, GWF, Protection. |
| **5** | EXTRA_ATTACK | PASSIVE | - | Attack twice per Action. |
| **6** | AURA_PROT | PASSIVE | - | Radius 3m; Adds CHA to all Saving Throws. |
| **10** | AURA_COURAGE | PASSIVE | - | Radius 3m; Immue to Frightened condition. |
| **11** | IMP_SMITE | PASSIVE | - | Permanent +1d8 Radiant to all melee hits. |

---

## Matrix B: Paladin Hub (Optimization Biases)

| Subclass_ID | Role | Transformation | Theme | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **VENGEANCE** | Pure DPR | Vow of Enmity | Retribution | **GOD_TIER (Accuracy)** |
| **ANCIENTS** | Hybrid Tank | Aura Warding | Nature | **S_TIER (Sustain)** |
| **OATHBREAKER**| Necro DPS | Aura of Hate | Darkness | **S_TIER (Burst)** |
| **DEVOTION** | Support / Acc | Sacred Weapon | Heroic | **A_TIER (Thematic)** |
| **CROWN (P8)** | Zone Tank | Champ Challenge| Duty | **A_TIER (Protection)**|

---

## Matrix C: Scaling Registry (Smites & Auras)

| Level | Smite_Max_Dmg | Lay_on_Hands | Aura_Range | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **2** | 2d8 | 3 charges | - | [Wiki](https://bg3.wiki/wiki/Paladin) |
| **6** | 4d8 (L3 Slot) | 7 charges | 3m | [Wiki](https://bg3.wiki/wiki/Paladin) |
| **10** | 5d8 (L4 Slot) | 11 charges | 3m | [Wiki](https://bg3.wiki/wiki/Paladin) |
| **12** | 5d8 + 1d8 | 13 charges | 3m | [Wiki](https://bg3.wiki/wiki/Paladin) |

---

## Matrix G: Subclass Progression Registry (Batch 1)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **DEVOTION** | 3 | **SACRED_WEPN** | ACTION | Add CHA mod to Attack Rolls (10 turns). |
| **DEVOTION** | 3 | **TURN_UNHOLY** | ACTION | Turn nearby Fiends and Undead. |
| **DEVOTION** | 7 | **AURA_DEVOT** | PASSIVE | Radius 3m; Allies cannot be Charmed. |
| **ANCIENTS** | 3 | **HEAL_RAD** | BONUS | AOE Heal pulse (2x) based on PB + CHA + Lvl. |
| **ANCIENTS** | 3 | **NAT_WRATH** | ACTION | Ensnare a target (STR save). |
| **ANCIENTS** | 7 | **AURA_WARD** | PASSIVE | Radius 3m; Resistance to SPELL damage. |
| **VENGEANCE** | 3 | **VOW_ENMITY** | BONUS | Advantage on attacks (Cast on self for global).|
| **VENGEANCE** | 3 | **ABJURE_ENEM** | ACTION | Frighten and Slow enemies. |
| **VENGEANCE** | 7 | **RE_AVENGER** | PASSIVE | Gain +4.5m speed after an Opportunity Attack. |
| **CROWN_P8** | 3 | **CHAMP_CHALL** | ACTION | Enemies cannot move > 9m from you. |
| **CROWN_P8** | 3 | **TURN_TIDE** | ACTION | Heal all allies (Prof + CHA + Lvl). |
| **CROWN_P8** | 7 | **DIVINE_ALLEGI**| REACT | Take damage for an ally within 3m. |
| **OATHBREAKER**| 3 | **CTRL_UNDEAD** | ACTION | Control Undead target (WIS save). |
| **OATHBREAKER**| 3 | **DREAD_ASPECT**| ACTION | Frighten nearby enemies. |
| **OATHBREAKER**| 3 | **SPITE_SUFFER**| ACTION | Target takes 1d4+CHA Necro per turn. |
| **OATHBREAKER**| 7 | **AURA_HATE** | PASSIVE | Radius 3m; +CHA to weapon damage (Fiend/Undead).|

---

## Matrix E: Selection Pool Matrix (Full Forensic Pools)

| Pool_ID | Choice_ID | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- |
| **CORE_SPELL**| **Shield of Faith** | **S** | +2 AC (BA); Essential for un-hittable tank builds. |
| **CORE_SPELL**| **Wrathful Smite** | **S** | Damage + Frightened; Best control smite. |
| **CORE_SPELL**| **Bless** | **S** | Global Accuracy/Save buff; Always high value. |
| **CORE_SPELL**| **Thunderous Smite**| **A** | Damage + Prone; Excellent for melee advantage. |
| **CORE_SPELL**| **Searing Smite** | **A** | Consistent Fire damage over time. |
| **CORE_SPELL**| **Divine Favour** | **A** | Efficient 1d4 Radiant per hit for 10 turns. |
| **CORE_SPELL**| **Aid** | **A** | Max HP increase; No concentration. |
| **CORE_SPELL**| **Warden Vitality**| **A** | 10 rounds of BA healing; Now castable with Level 4-6 slots. |
| **CORE_SPELL**| **Elemental Wpn** | **A** | +1 Atk; Now includes upcast benefits (+d6 at L5; +2d4 at L6). |
| **CORE_SPELL**| **Magic Weapon** | **B** | +1 Accuracy/Damage; Good if gear is weak. |
| **CORE_SPELL**| **Heroism** | **B** | Temp HP + Frightened immunity. |
| **CORE_SPELL**| **Revivify** | **B** | Mandatory safety net for Honour Mode. |
| **STYLE** | Defense | **S** | +1 AC; Synergizes with heavy armor/shields. |
| **STYLE** | Duelling | **A** | +2 Dmg for 1H weapon (Highest Sword/Board DPR).|
| **STYLE** | GWF | **A** | Reroll 1s/2s on Greatswords (Smite DPR max). |
| **STYLE** | Protection | **B** | Impose Disadv via Reaction; Shield required. |

---

## Matrix E2: Full Oath Spell Matrix (Forensic)

| Level | Devotion | Ancients | Vengeance | Oathbreaker | Crown (P8) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **3** | Prot Evil, Sanct | Speak Anim, Ensnar| Bane, Hunter Mark | Hellish Reb, Inflict| Command, Duel |
| **5** | Lesser Rest, Sil | Misty St, Moonbeam | Hold Pers, Misty St| Cr. Madness, Dark | Hold Pers, Ward B.|
| **9** | Beacon, Rem Curse | Plant Gr, Prot Ener| Haste, Prot Ener | Anim Dead, Bestow | Aura Vit, Spirit G |
| **13** | Death W, Freedom | Ice St, Fire Shield| Blight, Dim. Door | Blight, Confuse | Guard Faith, Death |

---

## Matrix D: Synergy DNA (Agent-Reasoning)

| Tag_ID | Optimization_Trigger | Satiation_Status | Logic_Anchor |
| :--- | :--- | :--- | :--- |
| **SMITE_NOVA** | Paladin 2 + Sorcerer 10 + Savage Attacker. | **SATIATED** | Matrix F |
| **INFINITE_ACC** | Vengeance Paladin + Self-Vow + GWM. | **SATIATED** | Matrix F |
| **WARD_TANK** | Ancients Paladin 7 + Warding Bond synergy. | **SATIATED** | Matrix F |
| **GISH_BARD** | Paladin 2 + Swords Bard 10 (Slashing Flourish). | **SATIATED** | Matrix F |

---

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Nova Threshold**: Paladins should hold high-level slots for critical hits to maximize `Divine Smite` efficiency.
> - **Vow Exploitation**: Always cast `Vow of Enmity` on **self** to gain global advantage against all targets for 10 turns.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "PALADIN_V13.2",
  "manifest_ref": "vanguard_manifest.json#PALADIN",
  "patch_baseline": "8_HOTFIX36",
  "building_priorities": {
    "stat_weight": {"STR": 1.0, "CHA": 0.8, "CON": 0.6},
    "multiclass_dips": {
      "Sorcerer_Blue": "Shield_Spell_Slot_Access",
      "Warlock_PotB": "Triple_Attack_Extra_Stacking_Bug_Fix"
    },
    "feat_ranking": ["GWM", "Savage_Attacker", "Alert", "Ability_Improvement"]
  },
  "multiclass_logic": {
    "slot_rounding": "FLOOR(lv_paladin / 2)",
    "nova_threshold": "PB_PLUS_CHA",
    "aura_priority": "CHA_MAX_20"
  },
  "tactical_exploits": {
    "vow_of_enmity": "SELF_CAST_FOR_GLOBAL_ADVANTAGE",
    "divine_smite_reaction": "CRIT_ONLY_TOGGLE"
  }
}
```


