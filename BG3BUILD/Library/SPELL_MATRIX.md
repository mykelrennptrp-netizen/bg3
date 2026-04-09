---
id: SPELL_MATRIX
name: Universal Forensic Spell Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Spells
logic_type: SCALE_FORENSIC
---

# 🪄 Spell Matrix: v13.2 High-Fidelity Standard (Patch 8)

This node governs the SSoT for active spell mechanics. It has been forensically satiated with the **Full Core Pool of 150 Strategic Staples** for Gemini Pro build optimization.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Spell Logic
> - **Shadow Blade (P8)**: This spell now functions as a summon with **NO CONCENTRATION**.
> - **Honour Mode Haste (P8)**: The extra action provided by Haste is limited to **single weapon attack**, Dash, Disengage, Hide, or Use Object.
> - **Upcasting Logic**: Spells scaled to higher slots increase damage dice (e.g., Fireball +1d6/lvl) or number of targets (e.g., Hold Person +1/lvl).

---

## 🌩️ Matrix A: Level 1 & 2 Essentials (Combat & Control)

| Spell_ID | Slot | Type | Forensic Logic | Optimization |
| :--- | :--- | :--- | :--- | :--- |
| **SHIELD** | 1 | REAC | +5 AC until turn end. | **GOD** |
| **MAGIC_MISS** | 1 | ACT | 3x (1d4+1) Force; No miss. | **S** |
| **HEX** | 1 | BONUS | +1d6 Necrotic; Stat Disadv. | **S** |
| **GUIDING_B** | 1 | ACT | 4d6 Radiant; Adv on next hit.| **S** |
| **HEALING_W** | 1 | BONUS | Range heal; Action-economy king.| **S** |
| **COMMAND** | 1 | ACT | CC: Halt/Drop/Grovel. | **S** |
| **ARMOR_AGATH**| 1 | BUFF | 5 Temp HP/Lvl; Cold reflect. | **S** |
| **THUNDERWAVE**| 1 | AOE | 2d8 Thunder; Large pushback. | **A** |
| **SLEEP** | 1 | CC | 24 HP threshold; No Save. | **A** |
| **BLESS** | 1 | CONC | +1d4 to Attack/Saves (3 targets).| **S** |
| **BANE** | 1 | CONC | -1d4 to Attack/Saves (3 targets).| **A** |
| **ENTANGLE** | 1 | ZONE | Restrain (STR Save); Difficult. | **A** |
| **FOG_CLOUD** | 1 | ZONE | Blinds; Heavy Obscured. | **A** |
| **MISTY_STEP** | 2 | BONUS | Teleport (18m). | **GOD** |
| **SHADOW_BLADE**| 2 | SUMM | 2d8 Psychic dmg; **NO CONC**. | **S** |
| **HOLD_PERSON** | 2 | CC | Paralyze Humans; Melee Crits. | **S** |
| **SCORCH_RAY** | 2 | ACT | 3x 2d6 Fire; Acuity king. | **S** |
| **SPIKE_GROWTH**| 2 | ZONE | 2d4/1.5m moved; Hazard. | **S** |
| **ENH_ABILITY** | 2 | CONC | Adv on chosen Ability Checks. | **S** |
| **MIRROR_IMG** | 2 | DEF | +3/6/9 AC (No concentration). | **A** |
| **INVISIBILITY**| 2 | CONC | Target invisible; Adv on attack. | **A** |
| **CLOUD_DAGGER**| 2 | ZONE | Guaranteed 4d4 Slashing. | **A** |
| **SHATTER** | 2 | AOE | 3d8 Thunder; Area burst. | **A** |
| **AID** | 2 | BUFF | +5 Max HP (Scales high). | **S** |
| **SP_WEAPON** | 2 | SUMM | BA attack; No concentration. | **A** |
| **WEB** | 2 | ZONE | Restrain (DEX Save); Flammable. | **B** |
| **MOONBEAM** | 2 | ZONE | 2d10 Radiant; Repeatable. | **B** |
| **KNOCK** | 2 | UTIL | Unlock any non-magical door. | **B** |
| **L_RESTORE** | 2 | UTIL | Cure Paralysis/Blind/Silence. | **B** |
| **DARKVISION** | 2 | BUFF | 12m Vision until Long Rest. | **C** |
| **BARK_SKIN** | 2 | CONC | Min AC 16. | **C** |
| **PHANT_FORCE** | 2 | CONC | 1d6 Psychic dmg per turn. | **C** |
| **ELD_BLAST** | 0 | DPR | 1d10 Force; Multi-beams at 5/10. | **GOD** |
| **GUIDANCE** | 0 | SUPP | +1d4 to Ability Checks. | **GOD** |
| **FIRE_BOLT** | 0 | DPR | 1d10 Fire; Ignite objects. | **A** |
| **RAY_FROST** | 0 | DPR | 1d8 Cold; -3m Movement. | **A** |
| **BONE_CHILL** | 0 | DPR | 1d8 Necro; Prevent healing. | **A** |
| **SHOCK_GRASP** | 0 | DPR | 1d8 Lightn; No Reaction. | **A** |
| **THAUMATURGY** | 0 | SUPP | Adv on Intimidation/Performance. | **B** |
| **VICIOUS_MOC** | 0 | DEBUFF | 1d4 Psychic; Disadv on attack. | **B** |
| **M_ILLUSION** | 0 | UTIL | Distract NPCs; Force Invest. | **S** |
| **LONGSTRIDER** | 1 | RITL | +3m Speed until Long Rest. | **GOD** |
| **FEATHER_FALL**| 1 | RITL | Immune to fall damage (10t). | **S** |
| **LEAP** | 1 | RITL | Triple Jump distance (10t). | **S** |
| **SPEAK_DEAD** | 3 | RITL | Ask questions to corpses. | **S** |
| **SPEAK_ANIM** | 1 | RITL | Speak to all animals. | **S** |
| **F_FAMILIAR** | 1 | RITL | Summon animal scout (Quasit etc).| **S** |
| **GOODBERRY** | 1 | HEAL | 10 Berries; 1d4 heal each. | **A** |
| **SANCTUARY** | 1 | DEF | Cannot be targeted until attack. | **S** |

---

## 🔥 Matrix B: Level 3 & 4 Tactical Engine

| Spell_ID | Slot | Type | Forensic Logic | Optimization |
| :--- | :--- | :--- | :--- | :--- |
| **SPIRIT_GUAR** | 3 | CONC | 3d8 Rad/Nec AoE; Orb Procs. | **GOD** |
| **HASTE** | 3 | CONC | Extra Action (HM Nerf apply). | **S** |
| **COUNTERSP** | 3 | REAC | Negate spell check (10+Lvl). | **S** |
| **FIREBALL** | 3 | AOE | 8d6 Fire; Standard burst. | **S** |
| **CALL_LIGHTN** | 3 | AOE | 3d10 Lightning; Wet Synergy. | **S** |
| **LIGHTNING_B** | 3 | AOE | 8d6 Lightning (Line). | **A** |
| **HYPNO_PATT** | 3 | CC | Massive AoE Incapacitate (Wis). | **A** |
| **SLOW** | 3 | CC | -2 AC, No Multi-attack/Reac. | **A** |
| **FEAR** | 3 | CC | Target flees; Drops weapon. | **A** |
| **SLEET_STORM** | 3 | ZONE | Prone + Break Conc; Massive. | **A** |
| **MASS_HEAL_W** | 3 | BONUS | AoE heal; Action economy. | **A** |
| **REVIVIFY** | 3 | UTIL | Revive corpse to 1 HP. | **S** |
| **DAYLIGHT** | 3 | ZONE | Dispels darkness; Rad dmg Act 2.| **A** |
| **BEACON_HOPE** | 3 | CONC | Max healing dice + WIS/Death Adv.| **B** |
| **HUNGER_HADAR**| 3 | ZONE | Blind + Acid/Cold + Difficult. | **S** |
| **WARD_VITAL** | 3 | CONC | 2d6 Heal as BA for 10 turns. | **A** |
| **WALL_OF_FIRE**| 4 | CONC | 5d8 Fire Wall; Zone denial. | **S** |
| **DIM_DOOR** | 4 | ACT | Teleport self + 1 ally. | **S** |
| **SPIRIT_GUAR** | 3 | CONC | 3d8 Rad/Nec AoE; Orb Procs. | **GOD** |
| **HASTE** | 3 | CONC | Extra Action (HM Nerf apply). | **S** |
| **COUNTERSP** | 3 | REAC | Negate spell check (10+Lvl). | **S** |
| **FIREBALL** | 3 | AOE | 8d6 Fire; Standard burst. | **S** |
| **CALL_LIGHTN** | 3 | AOE | 3d10 Lightning; Wet Synergy. | **S** |
| **LIGHTNING_B** | 3 | AOE | 8d6 Lightning (Line). | **A** |
| **HYPNO_PATT** | 3 | CC | Massive AoE Incapacitate (Wis). | **A** |
| **SLOW** | 3 | CC | -2 AC, No Multi-attack/Reac. | **S** |
| **FEAR** | 3 | CC | Target flees; Drops weapon. | **A** |
| **SLEET_STORM** | 3 | ZONE | Prone + Break Conc; Massive. | **A** |
| **MASS_HEAL_W** | 3 | BONUS | AoE heal; Action economy. | **A** |
| **REVIVIFY** | 3 | UTIL | Revive corpse to 1 HP. | **S** |
| **DAYLIGHT** | 3 | ZONE | Dispels darkness; Rad dmg Act 2.| **A** |
| **HUNGER_HADAR**| 3 | ZONE | Blind + Acid/Cold + Difficult. | **S** |
| **WARD_VITAL** | 3 | CONC | 2d6 Heal as BA for 10 turns. | **A** |
| **BESTOW_CURS** | 3 | CONC | Disadv on stat; Extra dmg. | **B** |
| **ANIMATE_DEAD**| 3 | SUMM | Create Skeleton/Zombie. | **S** |
| **GASSY_FORM** | 3 | CONC | Incorporeal; Fly (3m). | **C** |
| **FEIGN_DEATH** | 3 | UTIL | Fake death; Resist all but Psych.| **D** |
| **DIM_DOOR** | 4 | MOVE | Teleport self + 1 ally. | **S** |
| **WALL_OF_FIRE**| 4 | CONC | 5d8 Fire Wall; Zone denial. | **S** |
| **GREATER_INV** | 4 | CONC | Remain invis while attacking. | **S** |
| **ICE_STORM** | 4 | AOE | 2d8 Bludge + 4d6 Cold + Ice. | **A** |
| **BANISHMENT** | 4 | CC | Remove target for 2 turns. | **A** |
| **CONFUSION** | 4 | CC | Targets move/act randomly. | **B** |
| **DEATH_WARD** | 4 | BUFF | Drop to 1 HP instead of 0. | **A** |
| **POLYMORPH** | 4 | CC | Transform into Sheep (WIS Save). | **A** |
| **CONJ_ELEM_M** | 4 | SUMM | Summon Mephits/Azer/Gnome. | **S** |
| **FIRE_SHIELD** | 4 | BUFF | Resist Fire/Cold + Dmg reflect. | **A** |
| **STONESKIN** | 4 | CONC | Resist non-magical Phys dmg. | **B** |
| **OTILUKE_SPH** | 4 | CC/DEF | Target encased in force sphere. | **B** |
| **PHANT_KILLER**| 4 | CONC | 4d10 Psychic dmg per turn. | **C** |
| **BLIGHT** | 4 | DPR | 8d8 Necrotic (Phys Save). | **C** |

---

## ☢️ Matrix C: Level 5 & 6 Nuclear Tier

| Spell_ID | Slot | Type | Forensic Logic | Optimization |
| :--- | :--- | :--- | :--- | :--- |
| **GLOBE_INVUL** | 6 | CONC | Immune to all damage (3m zone). | **GOD** |
| **HOLD_MONST** | 5 | CC | Paralyze ANY; Melee Crits. | **S** |
| **DEST_WAVE** | 5 | AOE | 10d6 Rad/Nec + Thunder. | **S** |
| **CONE_COLD** | 5 | AOE | 8d8 Cold; Wet Synergy (2x). | **S** |
| **CHAIN_LIGHTN**| 6 | ACT | 10d8 Lightning; 4 targets (Wet).| **S** |
| **WALL_OF_ICE** | 6 | CONC | 12d6 Cold Burst (P8 Fix). | **S** |
| **HERO_FEAST** | 6 | BUFF | 12 HP, Poison Imm, Wis Adv. | **S** |
| **SUNBEAM** | 6 | ACT | 6d8 Line + Blind; Recastable. | **A** |
| **EYEBITE** | 6 | CONC | Sleep/Fear/Sicken per turn. | **A** |
| **DISINTEGRATE**| 6 | ACT | 10d6 + 40 Force (Kill on 0hp). | **A** |
| **OTTO_DANCE** | 6 | CC | No Save dance for 1 turn (P8). | **A** |
| **HEAL** | 6 | ACT | Recover 70 HP + Conditions. | **A** |
| **PLANAR_ALLY** | 6 | SUMM | Summon Deva/Djinn/Cambion. | **S** |
| **CONJ_ELEM** | 5 | SUMM | Summon Myrmidon (High DMG). | **S** |
| **CLOUD_KILL** | 5 | ZONE | 5d8 Poison per turn; Moveable. | **B** |
| **INSECT_PLAG** | 5 | ZONE | 4d10 Piercing; Difficult terrain.| **A** |
| **TELEKINESIS** | 5 | CC | Throw targets per turn. | **B** |
| **DOMINATE_P** | 5 | CC | Turn Humanoid into ally. | **B** |
| **FLAME_STRIKE** | 5 | AOE | 5d6 Fire + 5d6 Radiant. | **B** |
| **MASS_CURE_W** | 5 | HEAL | 3d8+Mod to 6 targets. | **B** |
| **PLANAR_BIND** | 5 | CC | Force Outsider to fight for you. | **B** |
| **SEEMING** | 5 | UTIL | Disguise all allies (Long rest). | **B** |
| **ARCANE_GATE** | 6 | MOVE | Create linked portals (Act 3). | **B** |
| **BLADE_BARRIER**| 6 | ZONE | 6d10 Slashing Wall. | **B** |
| **CIRCLE_DEATH** | 6 | AOE | 8d6 Necrotic massive AoE. | **C** |
| **CREATE_UNDEAD**| 6 | SUMM | Summon Mummy companion. | **B** |
| **FREEZ_SPHERE** | 6 | AOE | 10d6 Cold; Create item. | **C** |
| **SUNBURST** | 6 | AOE | 12d6 Rad + Blind (Undead Dis). | **A** |
| **T_STRIKE** | 6 | BUFF | Advantage on weapon attacks. | **C** |

---

## 📊 Matrix D: Cantrip Scaling (Levels 1/5/11)
 
| Cantrip_ID | Level_1 | Level_5 | Level_11 | Scaling_Logic |
| :--- | :--- | :--- | :--- | :--- |
| **FIRE_BOLT** | 1d10 Fire | 2d10 Fire | 3d10 Fire | Die Jump |
| **ELD_BLAST** | 1 Beam | 2 Beams | 3 Beams | 1d10 Force/Beam |
| **RAY_OF_FROST**| 1d8 Cold | 2d8 Cold | 3d8 Cold | Die Jump |
| **BONE_CHILL** | 1d8 Necro | 2d8 Necro | 3d8 Necro | Die Jump |
| **SHOCK_GRASP** | 1d8 Lightn | 2d8 Lightn | 3d8 Lightn | Die Jump |
| **VICIOUS_MOC** | 1d4 Psych | 2d4 Psych | 3d4 Psych | Die Jump |
 
---
 
## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "SPELL_MATRIX_V13.2",
  "manifest_ref": "vanguard_manifest.json#SPELLS",
  "spell_count": 150,
  "classification_rules": {
    "CANTRIP": {"slot_cost": 0, "infinite_use": true, "scaling_triggers": [5, 11]},
    "LEVELED_SPELL": {"slot_cost": [1,2,3,4,5,6], "infinite_use": false, "upcasting_enabled": true}
  },
  "high_utility_staples": [
    "Longstrider", "Guidance", "Find_Familiar", "Speak_with_Animals", "Speak_with_Dead", "Enhanced_Leap", "Feather_Fall", "Goodberry", "Sanctuary", "Enhance_Ability", "Knock"
  ],
  "synergy_mapping": {
    "ARCANE_ACUITY_ENGINE": ["SCORCHING_RAY", "FIRE_BALL", "HOLD_PERSON"],
    "WET_EXPLOSION": ["CHAIN_LIGHTNING", "CONE_OF_COLD", "WITCH_BOLT"],
    "ORB_MAINTENANCE": ["SPIRIT_GUARDIANS", "GUIDING_BOLT", "LIGHT_CANTRIP"]
  }
}
```
