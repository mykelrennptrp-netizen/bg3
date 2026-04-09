---
id: CLASS_FIGHTER
name: Fighter
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Fighter
primary_stat: [STR, DEX]
secondary_stat: CON
tertiary_stat: [INT, WIS]
hp_base: 10
hp_scaling: 6
armor_prof: [LIGHT, MEDIUM, HEAVY, SHIELDS]
weapon_prof: [SIMPLE, MARTIAL]
saving_throws: [STR, CON]
---

# ⚔️ Fighter: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate martial engine. It has been forensically satiated with the Octa-Matrix Standard, including **Arcane Archer (P8)** and full maneuver/shot selection pools.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Fighter Rules
> - **Extra Attack (Lv 5/11)**: Unique ability to attack 3 times per Action at level 11.
> - **Action Surge**: Grants a full additional Action (Once per Short Rest).
> - **War Magic Priority (P8)**: Eldritch Knights now execute all standard attacks *before* triggering the War Magic bonus action attack.
> - **Arcane Shot (P8)**: Magical projectiles that scale with Fighter level.

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | FIGHT_STYLE | SELECT | - | Select Fighting Style (Archery, Defense, etc.). |
| **1** | SECOND_WIND | BONUS | 1_PER_SR | Heal 1d10 + Fighter Level. |
| **2** | ACTION_SURGE | ACTION | 1_PER_SR | Gain 1 additional Action this turn. |
| **5** | EXTRA_ATTACK | PASSIVE | - | Attack twice per Action. |
| **6** | BONUS_FEAT | SELECT | - | Additional Feat/ASI selection (Fighter exclusive). |
| **9** | INDOMITABLE | PASSIVE | - | Reroll a failed Saving Throw (1 per LR). |
| **11**| IMP_EXTRA_ATT | PASSIVE | - | Attack **THREE** times per Action. |

---

## Matrix B: Fighter Hub (Building Biases)

| Subclass_ID | Role | Key Resource | Playstyle | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **BATTLE_MASTER**| Controller / DPR | Superiority Dice| Tactical | **GOD_TIER (Versatility)** |
| **ARCANE_ARCHER**| Magical Sniper | Arcane Shots | Ranged Control| **GOD_TIER (Ranged DPR)** |
| **ELD_KNIGHT** | Utility / Tank | Spell Slots | Hybrid | **S_TIER (Survival)** |
| **CHAMPION** | Crit Fisher | Passives | Simple / DPR | **A_TIER (Multi-Class)**|

---

## Matrix C: Scaling Registry (Resources)

| Level | Sup_Dice_Size | Sup_Dice_Count | Arcane_Shots | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **3** | 1d8 | 4 | 2 | [Wiki](https://bg3.wiki/wiki/Fighter) |
| **7** | 1d8 | 5 | 2 | [Wiki](https://bg3.wiki/wiki/Fighter) |
| **10** | 1d10 | 5 | 2 | [Wiki](https://bg3.wiki/wiki/Fighter) |

---

## Matrix G: Subclass Progression Registry (Granular)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **BATTLE_MASTER**| 3 | **SUPE_DICE** | PASSIVE | Gain 4d8 Superiority Dice. |
| **BATTLE_MASTER**| 3 | **MANEUVERS** | CHOICE | Gain 3 Maneuver selections. |
| **BATTLE_MASTER**| 7 | **MANEUVERS_2** | CHOICE | Gain 2 additional Maneuvers; +1 Die. |
| **BATTLE_MASTER**| 10| **IMPROVED_CD** | PASSIVE | Superiority Dice scale to 1d10. |
| **ARCANE_ARCH_P8**| 3 | **MAGIC_LORE** | PASSIVE | Gain Arcana or Nature proficiency. |
| **ARCANE_ARCH_P8**| 3 | **ARCANE_SHOT** | ACTION | Gain 2 uses/SR; Select 2 Shot types. |
| **ARCANE_ARCH_P8**| 7 | **MAGIC_ARROW** | PASSIVE | Non-magical arrows count as Magical. |
| **ARCANE_ARCH_P8**| 7 | **CURVING_SHOT** | BONUS | Reroll a missed attack against a new target. |
| **ARCANE_ARCH_P8**| 10| **ADD_SHIFT** | CHOICE | Gain 1 additional Arcane Shot selection. |
| **ELD_KNIGHT** | 3 | **WEAPON_BOND** | ACTION | Weapon cannot be disarmed; Returns when thrown.|
| **ELD_KNIGHT** | 3 | **SPELLCASTING** | PASSIVE | INT-based caster (1/3rd scaling). |
| **ELD_KNIGHT** | 7 | **WAR_MAGIC** | PASSIVE | Cast cantrip, then BA weapon attack. **P8 Fix**: Extra Attacks used first. |
| **ELD_KNIGHT** | 10| **ELD_STRIKE** | PASSIVE | Weapon hits give Disadv on enemy next save. |
| **CHAMPION** | 3 | **IMP_CRIT** | PASSIVE | Crit threshold reduced by 1 (19-20). |
| **CHAMPION** | 7 | **REM_ATHLETE** | PASSIVE | +0.5x Prof to STR/DEX/CON checks; Jump dist. |
| **CHAMPION** | 10| **ADD_FIGHTING** | CHOICE | Gain a second Fighting Style choice. |

---

## Matrix E: Selection Pool Matrix (Full Forensic Pools)

| Pool_ID | Choice_ID | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- |
| **MANEUVER** | Precision Attack | **S** | Adds to hit; Mandatory for GWM/Sharpshooter builds. |
| **MANEUVER** | Trip Attack | **S** | Inflicts Prone (Advantage for melee allies). |
| **MANEUVER** | Riposte | **S** | Best Reaction use; Attack on enemy miss. |
| **MANEUVER** | Menacing Attack | **A** | Inflicts Frightened; Excellent control. |
| **MANEUVER** | Disarming Attack| **A** | Forces enemy to drop weapon; Critical vs Martials. |
| **MANEUVER** | Pushing Attack | **A** | 4.5m shove; Elite battlefield positioning/ledge kills. |
| **MANEUVER** | Distracting | **B** | Next ally gets Adv; Situational support. |
| **MANEUVER** | Goading Attack | **B** | Forces target to hit you (Tanking). |
| **MANEUVER** | Maneuvering | **B** | Reposition ally without OAs. |
| **MANEUVER** | Feinting | **C** | Uses BA for Adv; Inferior to Precision. |
| **MANEUVER** | Commander/Rally | **C** | Niche support; Lower value in BG3 meta. |
| **MANEUVER** | Lunging/Sweeping| **D** | Range/AOE utility; Rarely optimal. |
| **ARC_SHOT** | Grasping Arrow | **S** | Ensnaring + 2d6 poison per move (DPR King). |
| **ARC_SHOT** | Bursting Arrow | **S** | 2d6 AOE Force damage. |
| **ARC_SHOT** | Banishment | **A** | Temporarily removes key threat from board. |
| **ARC_SHOT** | Seeking Arrow | **A** | Ignores cover/penalties; Guaranteed hit. |
| **ARC_SHOT** | Shadow Arrow | **B** | Blind effect; Good for control. |
| **ARC_SHOT** | Enfeeble/Pierce | **C** | Reduced damage / Line damage; Niche. |
| **STYLE** | Archery | **S** | +2 to Ranged Attack Rolls. |
| **STYLE** | Defense | **A** | +1 AC (Universal utility). |
| **STYLE** | Duelling | **B** | +2 Damage for 1H weapon (Good for Shields). |
| **STYLE** | TWF / GWF | **B** | Add mod to off-hand / Reroll 1s and 2s. |
| **STYLE** | Protection | **C** | Shield-based reaction; Inferior to Sentinel feat. |

---

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Action Surge Economy**: Action Surge is the premier single-turn multiplier. Always synchronize with `Haste` and `Elixir of Bloodlust` for maximum action saturation.
> - **Precision Priority**: For GWM/Sharpshooter builds, `Precision Attack` (Battle Master) or `Curving Shot` (Arcane Archer) are mandatory to maintain a >75% hit rate.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "FIGHTER_V13.2",
  "manifest_ref": "vanguard_manifest.json#FIGHTER",
  "patch_baseline": "8_HOTFIX36",
  "building_priorities": {
    "stat_weight": {"STR": 1.0, "DEX": 1.0, "CON": 0.8, "INT": 0.4},
    "multiclass_dips": {
      "Fighter_2": "Action_Surge_For_All",
      "Fighter_1": "Con_Save_Heavy_Armor_Start"
    },
    "feat_ranking": ["GWM", "Sharpshooter", "Savage_Attacker", "Alert"]
  },
  "subclass_logic": {
    "arcane_archer_p8": {"shots_per_rest": 2, "curving_shot_ba": true},
    "eldritch_knight_bound": {"returning_weapon": true, "disarm_immune": true},
    "battle_master_dc": "8 + Prof + STR/DEX"
  }
}
```


