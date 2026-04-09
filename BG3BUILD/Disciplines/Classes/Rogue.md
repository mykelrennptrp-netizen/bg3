---
id: CLASS_ROGUE
name: Rogue
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Rogue
primary_stat: DEX
secondary_stat: [CHA, INT]
tertiary_stat: CON
hp_base: 8
hp_scaling: 5
armor_prof: [LIGHT]
weapon_prof: [SIMPLE, HAND_XBOW, LONG_SWORD, RAPIER, SHORT_SWORD]
saving_throws: [DEX, INT]
---

# 🗡️ Rogue: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate precision striker. It has been forensically satiated with the Octa-Matrix Standard, including **Swashbuckler (P8)** and full expertise selection pools.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Rogue Rules
> - **Sneak Attack (SSoT)**: Add `floor(Level/2) + 1` d6 damage if you have Advantage or an ally is within 1.5m of the target. **Limits**: Once per Turn (NOT Round). **Fix**: Now triggers on additional projectiles (Curving Shot).
> - **Shadow Blade (P8)**: Shadow Blade (from ring) **NO LONGER REQUIRES CONCENTRATION**.
> - **Uncanny Dodge (P8)**: Now correctly triggers once per round; rogue cannot use it while **Incapacitated**. 
> - **Reliable Talent (Lv 11)**: Any roll of 9 or lower on a proficient skill check is treated as a **10**.
> - **Cunning Action**: Hide, Dash, and Disengage are **Bonus Actions**.

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | SNEAK_ATTACK | SPECIAL | - | Add 1d6 (Scales every odd level). |
| **1** | EXPERTISE_1 | SELECT | - | Double Proficiency Bonus in 2 chosen skills. |
| **2** | CUNNING_ACTION| BONUS | - | Dash, Disengage, or Hide as a Bonus Action. |
| **3** | SUBCLASS | SELECT | - | Thief, Assassin, Arcane Trickster, Swashbuckler.|
| **5** | UNCANNY_DODGE | REACT | - | Halve incoming attack damage once per round. |
| **6** | EXPERTISE_2 | SELECT | - | Double Proficiency Bonus in 2 additional skills.|
| **7** | EVASION | PASSIVE | - | Zero damage on successful DEX save vs Spells. |
| **11** | RELIABLE_TAL | PASSIVE | - | Minimum roll of 10 on all proficient checks. |

---

## Matrix B: Rogue Hub (Optimization Biases)

| Subclass_ID | Role | Key Strength | Playstyle | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **THIEF** | Action Economy | Fast Hands | Multi-Tasker | **GOD_TIER (DPR/Util)**|
| **ASSASSIN** | Alpha Striker | Assassinate | Stalker | **S_TIER (Ambush)** |
| **SWASH_P8** | Duelist | Rakish Audacity | Frontline | **S_TIER (Solo-Sneak)**|
| **ARC_TRICK** | Magic Thief | Magical Ambush | Controller | **A_TIER (CC)** |

---

## Matrix C: Sneak Attack Scaling Registry

| Level | Sneak_Dice | Avg_DPR_Gain | Expertise_PB | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **1** | 1d6 | 3.5 | +4 | [Wiki](https://bg3.wiki/wiki/Sneak_Attack) |
| **3** | 2d6 | 7.0 | +4 | [Wiki](https://bg3.wiki/wiki/Sneak_Attack) |
| **5** | 3d6 | 10.5 | +6 | [Wiki](https://bg3.wiki/wiki/Sneak_Attack) |
| **7** | 4d6 | 14.0 | +6 | [Wiki](https://bg3.wiki/wiki/Sneak_Attack) |
| **9** | 5d6 | 17.5 | +8 | [Wiki](https://bg3.wiki/wiki/Sneak_Attack) |
| **11** | 6d6 | 21.0 | +8 | [Wiki](https://bg3.wiki/wiki/Sneak_Attack) |

---

## Matrix G: Subclass Progression Registry (Granular)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **THIEF** | 3 | **FAST_HANDS** | PASSIVE | Gain an **ADDITIONAL BONUS ACTION**. |
| **THIEF** | 3 | **SECOND_STORY** | PASSIVE | Resistance to falling damage. |
| **THIEF** | 9 | **SUPREME_SNEAK**| ACTION | Become Invisible; Advantage on Stealth (Invis). |
| **ASSASSIN** | 3 | **ASS_AMBUSH** | PASSIVE | Auto-crit vs Surprised; Attack refund on start. |
| **ASSASSIN** | 3 | **ASS_INIT** | PASSIVE | Advantage vs creatures that haven't acted yet. |
| **ASSASSIN** | 9 | **INFIL_EXP** | ACTION | Change appearance to disguise yourself. |
| **SWASH_P8** | 3 | **FANCY_FOOT** | PASSIVE | Melee attack prevents enemy target from OA. |
| **SWASH_P8** | 3 | **RAKISH_AUD** | PASSIVE | Add CHA to Initiative; Solo-target Sneak Attack.|
| **SWASH_P8** | 9 | **PANACHE** | ACTION | Taunt target (Disadv on others) OR Charm non-host.|
| **SWASH_P8** | 11| **MASTER_DUEL** | PASSIVE | Reroll one missed attack per turn (Safety Net). |
| **ARC_TRICK** | 3 | **LEGERDEMAIN** | ACTION | Invisible Mage Hand (Pickpocket/Disarm). |
| **ARC_TRICK** | 9 | **MAG_AMBUSH** | PASSIVE | Targets have Disadv against your spells if hidden.|

---

## Matrix E: Selection Pool Matrix (Full Forensic Pools)

| Pool_ID | Choice_ID | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- |
| **EXPERTISE** | **Sleight of Hand**| **S** | Lockpicking/Pickpocketing primary engine. |
| **EXPERTISE** | **Stealth** | **S** | Essential for reliable Sneak Attack positioning. |
| **EXPERTISE** | **Perception** | **S** | Trap and hidden chest detection. |
| **EXPERTISE** | **Persuasion** | **S** | Critical for social-based dialog rolls. |
| **EXPERTISE** | **Athletics** | **A** | High-tier for Swashbucklers (Shove resistance). |
| **EXPERTISE** | **Insight** | **A** | Detecting lies in conversation. |
| **EXPERTISE** | **Deception** | **A** | Alternative social path for infiltrators. |
| **EXPERTISE** | **Acrobatics** | **B** | Resistance to being shoved; mobility. |
| **EXPERTISE** | **Investigation** | **B** | Finding clues and secret doors. |
| **EXPERTISE** | **Intimidation** | **B** | Brute-force social interaction. |
| **EXPERTISE** | **Performance** | **C** | Niche social distraction logic. |
| **EXPERTISE** | **Religion/Nature**| **C** | Lore-specific skill checks. |
| **EXPERTISE** | **Medicine** | **C** | Niche healing support checks. |
| **AT_SPELL** | **Shield** | **S** | Best defensive reaction for squishy rogues. |
| **AT_SPELL** | **Hold Person** | **S** | Guarantees critical sneak attacks. |
| **AT_SPELL** | **Tasha's Laught**| **A** | CC target (Prone) for melee advantage. |
| **AT_SPELL** | **Invisibility** | **A** | Ultimate infiltration and positioning tool. |
| **AT_SPELL** | **Mirror Image** | **A** | Concentration-free defensive layers. |
| **AT_SPELL** | **Sleep** | **B** | Low-level CC (No save); Strong in Act 1. |
| **AT_SPELL** | **Charm Person** | **B** | Social utility and combat avoidance. |
| **AT_SPELL** | **Disguise Self** | **B** | Infiltration and Speak with Dead synergy. |
| **AT_SPELL** | **Misty Step (Any)**| **S** | Best mobility spell (Use Any-School slot). |

---

## Matrix F: Build Synergy Biases (Agent-Logic)

| Synergy_ID | Component_A | Component_B | Logic_Goal |
| :--- | :--- | :--- | :--- |
| **DOUBLE_DIP** | Sneak Attack | Opportunity Atk | **Trigger Sneak Attack TWICE** per round. |
| **GLOOM_ASS** | Assassin 3 | Gloom Stalker 5 | Turn 1 wipe logic (Auto-Crit + Dread Ambusher). |
| **SOLO_SWASH** | Rakish Audacity | CHA Stacking | High Initiative + No-Advantage Sneak Attack. |
| **MAGE_SNEAK** | Magical Ambush | Hold Person | Use stealth to force failed saves + Auto-Crits. |

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Double-Dip Sneak Attack**: Use Reactions (Opportunity Attacks or Commander's Strike) to trigger Sneak Attack a second time in a round, as the limit is "Once per Turn."
> - **Master Duelist Lock**: At Lv 11, Swashbucklers effectively eliminate the risk of a "0-DPR" turn by rerolling any miss.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "ROGUE_V13.2",
  "manifest_ref": "vanguard_manifest.json#ROGUE",
  "patch_baseline": "8_HOTFIX36",
  "mechanics": {
    "reliable_talent_floor": 10,
    "sneak_attack_per_turn": 1,
    "sneak_attack_per_round_max": 2
  },
  "subclass_logic": {
    "thief_bonus_actions": 2,
    "swash_cha_to_init": true,
    "assassin_surprised_crit": true
  },
  "building_priorities": {
    "expertise_ranking": ["Sleight_Hand", "Stealth", "Perception", "Persuasion"],
    "at_spell_intelligence_req": 14
  }
}
```


