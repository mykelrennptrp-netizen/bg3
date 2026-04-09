---
id: CLASS_WARLOCK
name: Warlock
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Warlock
primary_stat: CHA
secondary_stat: CON
tertiary_stat: DEX
hp_base: 8
hp_scaling: 5
armor_prof: [LIGHT, MEDIUM, SHIELDS]
weapon_prof: [SIMPLE, MARTIAL]
saving_throws: [WIS, CHA]
---

# 🔮 Warlock: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate pact-bound agent. It has been forensically satiated with the Octa-Matrix Standard, including **Hexblade (P8)** and full Eldritch Invocation selection pools.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Warlock Rules
> - **Pact Magic (SSoT)**: Spells slots are always at the highest available level. Recover on **Short Rest**.
> - **Multiclass Rounding**: Warlock levels **DO NOT** contribute to multiclass spell slot levels. They remain separate resources.
> - **Blade Pact Extra Attack (P8)**: In **Standard/Tactician**, the Extra Attack from Pact of the Blade stacks with other Extra Attack features (3x Total). In **Honour Mode**, it does NOT stack.
> - **Eldritch Blast**: Scales by **Character Level**, not Warlock Level (Lv 5: 2 beams, Lv 10: 3 beams).

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | PATRON | SELECT | - | Select Fiend, Archfey, GOO, or Hexblade. |
| **2** | INVOCATIONS_1 | SELECT | - | Choose 2 Eldritch Invocations. |
| **3** | PACT_BOON | SELECT | - | Chain, Blade, or Tome. |
| **5** | DEEP_PACT | PASSIVE | - | Improved Pact; Adds Extra Attack to Blade. |
| **7** | INVOCATIONS_2 | SELECT | - | Choose 1 additional Invocation (Lv 7 reqs open).|
| **11** | MYSTIC_ARCAN | SELECT | - | Learn 1 Level 6 spell (Long Rest recovery). |
| **12** | INVOCATIONS_3 | SELECT | - | Choose final Invocation (**LIFEDRINKER**). |

---

## Matrix B: Warlock Hub (Optimization Biases)

| Subclass_ID | Role | Key Strength | Playstyle | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **HEXBLADE_P8** | Martial Brawler | Hex Warrior | Frontline Gish | **GOD_TIER (Melee)** |
| **FIEND** | Blaster / Tank | Temp HP on Kill | Aggressive | **S_TIER (DPR)** |
| **GOO** | Controller | Crit Fear | Sniper | **S_TIER (CC)** |
| **ARCHFEY** | Infiltrator | Misty Escape | Utility | **A_TIER (Utility)** |

---

## Matrix C: Scaling Registry (Pact Magic & EB)

| Level | Slot_Level | Slot_Count | EB_Beams | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **1** | 1 | 1 | 1 | [Wiki](https://bg3.wiki/wiki/Warlock) |
| **3** | 2 | 2 | 1 | [Wiki](https://bg3.wiki/wiki/Warlock) |
| **5** | 3 | 2 | 2 | [Wiki](https://bg3.wiki/wiki/Warlock) |
| **9** | 5 | 2 | 2 | [Wiki](https://bg3.wiki/wiki/Warlock) |
| **11** | 5 | 3 | 3 | [Wiki](https://bg3.wiki/wiki/Warlock) |

---

## Matrix G: Subclass Progression Registry (Granular)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **HEXBLADE_P8** | 1 | **HEX_WARRIOR** | PASSIVE | Use CHA for Attack/Dmg; Shield Proficiency. |
| **HEXBLADE_P8** | 1 | **HEX_CURSE** | BONUS | Prof Bonus to Dmg; 19-20 Crit; Heal on Kill. |
| **HEXBLADE_P8** | 6 | **ACC_SPECTER** | ACTION | Raise Specter from corpse (Once per LR). |
| **HEXBLADE_P8** | 10| **ARM_HEXES** | REACT | Roll d6 on hit; 4+ forces the hit to miss. |
| **FIEND** | 1 | **D_ONE_BLESS** | PASSIVE | Gain [CHA + Lvl] Temp HP when killing enemy. |
| **FIEND** | 6 | **D_ONE_LUCK** | ACTION | Add 1d10 to an Ability Check or Saving Throw. |
| **FIEND** | 10| **FIEND_RESIL** | PASSIVE | Gain Resistance to one damage type (Switchable).|
| **GOO** | 1 | **MORTAL_REM** | PASSIVE | Critical Hits Frighten target and nearby enemies.|
| **GOO** | 6 | **ENTROPIC_W** | REACT | Impose Disadv on attack; your next attack Adv. |
| **GOO** | 10| **THOUGHT_SHLD**| PASSIVE | Resistant to Psychic; Reflect Psychic dmg. |

---

## Matrix E: Selection Pool Matrix (Full Forensic Pools)

| Pool_ID | Choice_ID | Lv_Req | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- | :--- |
| **INVOCATION** | **Agonizing Blast**| - | **S** | Add CHA to Eldritch Blast damage (DPR King). |
| **INVOCATION** | **Repelling Blast**| - | **S** | Push targets 4.5m; Infinite gravity kills. |
| **INVOCATION** | **Devil's Sight** | - | **S** | See in Magical Darkness (Darkness Combo). |
| **INVOCATION** | **Lifedrinker** | 12 | **S** | Add CHA Necrotic dmg to melee (Blade King). |
| **INVOCATION** | **Armour Shadows**| - | **A** | Free Mage Armour; 13+DEX AC for Sorlocks. |
| **INVOCATION** | **Minions Chaos** | 9 | **A** | Summon Elemental using Pact Slot. |
| **INVOCATION** | **Otherworld Leap**| 9 | **B** | Infinite Jump (Ritual); Extreme mobility. |
| **INVOCATION** | **Slow** | 5 | **B** | Cast Slow using Pact Slot (Control boost). |
| **INVOCATION** | **Misty Visions** | - | **B** | Infinite Silent Image; Stealth/Distraction tool.|
| **INVOCATION** | **Mask Many Face** | - | **B** | Infinite Disguise Self (Speak w/ Dead utility). |
| **INVOCATION** | **Beast Speech** | - | **C** | Infinite Speak with Animals. |
| **INVOCATION** | **Gaze Two Minds** | - | **C** | Psychic link with ally (Niche social). |
| **BOON** | **Pact of Blade** | 3 | **S** | Bound weapon uses CHA; Extra Attack at Lv 5. |
| **BOON** | **Pact of Tome** | 3 | **S** | Haste/Call Lightning at Lv 5; Best for Casters.|
| **BOON** | **Pact of Chain** | 3 | **B** | Imp/Quasit for invis-scouting and extra BA. |

---

## Matrix E2: Patron Spell Matrix (Forensic)

| Level | Fiend | GOO | Archfey | Hexblade (P8) |
| :--- | :--- | :--- | :--- | :--- |
| **1** | Command, Burning H| Tasha, Diss Whis | Faerie Fire, Sleep | Shield, Wrathful Sm|
| **2** | Scorching, Blind | Phant F, Detect T | Phant F, Calm Em | Blur, Brand Smite |
| **3** | Fireball, Stink C | Fear, Bestow Cur | Blink, Plant Gr | Blink, Elem Weapon |
| **4** | Wall Fire, Fire S | Dom Beast, Black T| Dom Beast, Gr Inv | Phant Kill, Stagger|
| **5** | Flame St, Cone C | Dom Person, Telek| Dom Person, Seem | Banishing Sm, Cone |

---

## Matrix F: Build Synergy Biases (Agent-Logic)

| Synergy_ID | Component_A | Component_B | Logic_Goal |
| :--- | :--- | :--- | :--- |
| **TRIPLE_ATTACK**| Pact Blade 5 | Martial 5 (Non-HM)| **3 Attacks per Action** (Tactician/Std). |
| **DARKNESS_DS** | Darkness Spell | Devil's Sight | Pure Advantage + Untargetability zone. |
| **HEX_SMITE** | Hexblade | Paladin 2 | CHA-based Smites with 19-20 Crit threshold. |
| **FORCE_GATLING**| Eldritch Blast | Agonizing Blast | 3 beams x [d10+CHA+PB] with Potent Robe. |

### [TACTICAL] Hex Warrior Accuracy
- **CHA SAD**: By using Charisma for both Spells and Melee, Warlocks only need **DEX 14** and **CON 16**, allowing for **CHA 20** + feats like *Alert* or *GWM*.

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Hexblade SAD Execution**: Hexblades use CHA for both melee and spells. This allows for a "Pure CHA" build path, freeing up points for `CON` and `DEX` (AC).
> - **Double-Dip Extra Attack**: In non-Honour modes, ensure Warlock 5 + Paladin/Fighter 5 is achieved to exploit the 3-attack stacking logic.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "WARLOCK_V13.2",
  "manifest_ref": "vanguard_manifest.json#WARLOCK",
  "patch_baseline": "8_HOTFIX36",
  "hexblade_p8": {
    "hex_warrior_stats": ["CHA_to_Atk", "CHA_to_Dmg"],
    "is_medium_armor_prof": true,
    "is_shield_prof": true
  },
  "building_priorities": {
    "stat_weight": {"CHA": 1.0, "CON": 0.8, "DEX": 0.6},
    "multiclass_dips": {
      "Paladin_7": "Smite_Aura_Synergy",
      "Sorcerer_10": "Sorlock_Machine_Gun"
    },
    "invocation_ranking": ["Agonizing_Blast", "Repelling_Blast", "Devil_Sight", "Lifedrinker"],
    "blade_pact_stacking_hm": false
  }
}
```
