---
id: CLASS_WIZARD
name: Wizard
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Wizard
primary_stat: INT
secondary_stat: CON
tertiary_stat: DEX
hp_base: 6
hp_scaling: 4
armor_prof: NONE
weapon_prof: [DAGGER, QUARTERSTAFF, LIGHT_XBOW]
saving_throws: [INT, WIS]
---

# 🧙‍♂️ Wizard: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate arcane scholar. It has been forensically satiated with the Octa-Matrix Standard, including **Bladesinging (P8)** and full spell-scribing cost matrices.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Wizard Rules
> - **Arcane Recovery (SSoT)**: Recover spell slots equal to `floor(Level/2)` once per Long Rest outside of combat. **Limit**: Cannot recover Level 6 slots.
> - **Scribing (P8)**: Can learn ANY spell from a scroll if you have a spell slot of that level. Cost: 50gp per spell level (reduced for school specialty). **Fix**: Level 6 scrolls now correctly appear in vendor inventories more frequently.
> - **Bladesong (P8)**: Gain Bonus to AC and Concentration saves equal to INT mod. Only active while wearing Light or No armor.
- **Arcane Recovery**: Recover spell slots outside of combat. **Limit**: Total Slot Levels <= Wizard Level. **Restriction**: Cannot recover Level 6 slots.
- **Bladesinging (P8)**: 
    - **Bladesong**: +INT to AC, +3m Speed, Adv on Acrobatics, +INT to Conc. Requires No Shield/Medium/Heavy Armor.
    - **Extra Attack (Lv 6)**: Can replace one weapon attack with a Cantrip (Beguiler/Shocking/Ward).

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | ARC_RECOVERY | ACTION | 1_REST | Recover spell slots up to Wizard Lvl. |
| **1** | SCRIBING | ACTION | GOLD | Learn permanent spells from scrolls. |
| **2** | SUBCLASS | SELECT | - | Select 1 of 8 Schools or Bladesinging. |
| **6** | SUB_FEAT_6 | PASSIVE | - | Bladesinger Extra Atk / School Power Spike. |
| **10** | SUB_FEAT_10 | PASSIVE | - | Song of Defense / Final School Feature. |

---

## Matrix B: Wizard Hub (Optimization Biases)

| Subclass_ID | Role | Key Strength | Playstyle | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **ABJURATION** | Pure Tank | Arcane Ward | Immortality | **GOD_TIER (Sustain)**|
| **BLADESING_P8**| Gish / Melee | INT-to-AC | Duelist | **GOD_TIER (DPR)** |
| **DIVINATION** | RNG Control | Portent | Oracle | **S_TIER (Control)** |
| **EVOCATION** | Blaster | Sculpt Spells | Safety | **S_TIER (Damage)** |
| **NECROMANCY** | Summoner | Undead Thralls | Commander | **S_TIER (Econ)** |
| **ENCHANTMENT** | Crowd Control | Split Enchant | Puppet Master | **A_TIER (CC)** |
| **ILLUSION** | Stealth / Dist | Illusory Self | Trickster | **B_TIER (Utility)** |
| **TRANSMUTE** | Support | Trans Stone | Alchemist | **B_TIER (Buffs)** |

---

## Matrix C: Scaling Registry (Recovery & Ward)

| Level | Recovery_Pts | Max_Slot_Recov | Ward_Cap | Portents | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **2** | 2 | 1 | 4 | 2 | [Wiki](https://bg3.wiki/wiki/Wizard) |
| **6** | 6 | 3 | 12 | 3 | [Wiki](https://bg3.wiki/wiki/Wizard) |
| **10** | 10 | 5 | 20 | 3 | [Wiki](https://bg3.wiki/wiki/Wizard) |
| **12** | 12 | 5 | 24 | 3 | [Wiki](https://bg3.wiki/wiki/Wizard) |

---

## Matrix G: Subclass Progression Registry (Full Forensic)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **ABJURATION** | 2 | **ARC_WARD** | PASSIVE | Damage reduction = Ward stacks (Max 2xLvl). |
| **ABJURATION** | 6 | **PROJ_WARD** | REACT | Use your Ward to reduce damage to an ally. |
| **ABJURATION** | 10| **IMP_ABJUR** | PASSIVE | Ward stacks = Wizard Lvl after Short Rest. |
| **BLADESING_P8**| 2 | **BLADESONG** | BONUS | Huge AC/Speed/Conc boost (No Shield/Armor). |
| **BLADESING_P8**| 6 | **CANTRIP_ATK**| PASSIVE | Replace 1 Extra Attack swing with a Cantrip. |
| **BLADESING_P8**| 10| **SONG_DEF** | REACT | Burn spell slot to reduce damage by 5xSlotLvl.|
| **DIVINATION** | 2 | **PORTENT** | SPECIAL | Replace any roll with a pre-rolled D20. |
| **DIVINATION** | 6 | **EXPERT_DIV** | PASSIVE | Regain Lv 1-5 slots when casting Divination. |
| **EVOCATION** | 2 | **SCULPT_SP** | PASSIVE | Allies automatically succeed saves vs your AOE.|
| **EVOCATION** | 10| **EMP_EVOC** | PASSIVE | Add INT mod to all Evocation spell damage. |
| **NECROMANCY** | 6 | **U_THRALLS** | PASSIVE | Extra Health/Dmg for Undead; Animate more. |
| **ENCHANTMENT** | 10| **SPLIT_ENCH** | PASSIVE | Target 2 creatures with single-target Enchant. |
| **ILLUSION** | 2 | **IMP_MINOR_I**| PASSIVE | Cast Minor Illusion as Bonus Action (+Invis). |
| **ILLUSION** | 10| **ILLUS_SELF** | REACT | Force an attack to miss you (1 per Short Rest).|
| **TRANSMUTE** | 6 | **TRANS_STONE**| ACTION | Create stone granting Prof: CON or Resist. |

---

## Matrix E: Selection Pool Matrix (Full Forensic Pools)

| **Level** | **Choice_ID** | **Tier** | **Optimization Logic** |
| :--- | :--- | :--- | :--- |
| **1** | **Shield** | **S** | Absolute survival necessity (Reaction AC). |
| **1** | **Magic Missile**| **A** | Reliable damage; Procs item-on-hit effects. |
| **2** | **Misty Step** | **S** | Premier positional utility. |
| **2** | **Hold Person** | **A** | Critical control for humanoid deletion. |
| **3** | **Fireball** | **S** | Standard AOE burst. |
| **3** | **Haste** | **S** | Multiplies striker action economy. |
| **3** | **Counterspell**| **S** | Magic denial reaction. |
| **4** | **Confusion** | **A** | Massive AOE disruption/CC. |
| **4** | **Ice Storm** | **A** | AOE Damage + Terrain control. |
| **5** | **Hold Monster** | **S** | Paralyze any creature for auto-crits. |
| **5** | **Conjure Elem** | **S** | High HP/DPR summon for action economy. |
| **6** | **Globe Invul** | **S** | Total immunity zone for boss mechanics. |
| **6** | **Wall of Ice** | **A** | Icy Cloud damage boosted to **10d6** (P8). |
| **6** | **Chain Lightn** | **A** | Elite multi-target burst. |

---

## Matrix F: Build Synergy Biases (Agent-Logic)

| Synergy_ID | Component_A | Component_B | Logic_Goal |
| :--- | :--- | :--- | :--- |
| **CANTRIP_BLADE**| Extra Attack | Shocking Grasp | Melee DPR + Removing enemy reactions. |
| **WARD_TANK** | Abjuration Lvl | Armour Agathys | High HP + Damage Reflection + Reduction. |
| **PORT_CC** | Portent (Low) | Hold Monster | Forced success on critical control spells. |
| **SCULPT_NUKE** | Sculpt Spells | Fireball | Dropping AOE on melee allies with 0 risk. |

### [TACTICAL] Arcane Endurance
- **Slot Recovery Lock**: Agent must verify `Slot_Level < 6`. Arcane Recovery cannot restore *Globe of Invulnerability* or *Disintegrate*.

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Scribing Utility**: Prioritize scribing utility spells (`Mist Step`, `Haste`) to free up "Preparation" slots for high-impact control spells.
> - **Abjuration Shield**: Abjurers should prioritize `Glyph of Warding` or `Armor of Agathys` (Multiclass) to rapidly build Arcane Ward stacks.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "WIZARD_V13.2",
  "manifest_ref": "vanguard_manifest.json#WIZARD",
  "patch_baseline": "8_HOTFIX36",
  "mechanics": {
    "arcane_recovery_limit": 5,
    "scribing_cost_base": 50,
    "scribing_cost_specialty": 25,
    "level_6_recovery_possible": false
  },
  "bladesinging_p8": {
    "ac_bonus": "INT_MOD",
    "conc_save_bonus": "INT_MOD",
    "speed_bonus": 3,
    "restriction": "NO_MEDIUM_HEAVY_ARMOR_OR_SHIELD"
  },
  "building_priorities": {
    "stat_weight": {"INT": 1.0, "CON": 0.8, "DEX": 0.6},
    "multiclass_dips": {
      "Cleric_1": "Heavy_Armor_Shield_Domain",
      "Fighter_2": "Action_Surge_Double_Fireball"
    },
    "feat_ranking": ["War_Caster", "Alert", "Ability_Improvement", "Dual_Wielder"]
  }
}
```
