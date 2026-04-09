---
id: CLASS_RANGER
name: Ranger
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Ranger
primary_stat: DEX
secondary_stat: WIS
tertiary_stat: CON
hp_base: 10
hp_scaling: 6
armor_prof: [LIGHT, MEDIUM, SHIELDS]
weapon_prof: [SIMPLE, MARTIAL]
saving_throws: [STR, DEX]
---

# 🏹 Ranger: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate survivalist. It has been forensically satiated with the Octa-Matrix Standard, including **Swarmkeeper (P8)**, **Drakewarden (P8)**, and full companion scaling stats.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Ranger Rules
> - **Favoured Enemy (SSoT)**: Grants skill proficiencies and spell/armor access. **Ranger Knight** is the ONLY path to Heavy Armor for Rangers.
> - **Natural Explorer**: Grants environmental utility or resistances.
> - **Pet Scaling (P8)**: All companions (Beast Master & Drake) inherit the Ranger's **Proficiency Bonus** to AC and Attack Rolls.
> - **Companion Mobility (P8)**: All Ranger companions can now **DASH** using either an **Action or a Bonus Action** (Massive positional buff).
> - **Extra Attack (Lv 5)**: Standard martial multi-attack.

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | FAVORED_ENEMY | SELECT | - | Select Bounty Hunter, Ranger Knight, etc. |
| **1** | NATURAL_EXPL | SELECT | - | Select Beast Tamer, Urban Tracker, etc. |
| **2** | FIGHT_STYLE | SELECT | - | Archery, Defense, Dueling, TWF. |
| **3** | SUBCLASS | SELECT | - | Hunter, Beast Master, Gloom, Swarm, Drake. |
| **5** | EXTRA_ATTACK | PASSIVE | - | Attack twice per Action. |
| **6** | FAVORED_ENEMY | SELECT | - | Gain second Favoured Enemy choice. |
| **6** | NATURAL_EXPL | SELECT | - | Gain second Natural Explorer choice. |
| **8** | LAND_STRIDE | PASSIVE | - | Difficult Terrain no longer slows movement. |
| **10** | HIDE_SIGHT | ACTION | - | Invisible + Stealth bonus until movement. |

---

## Matrix B: Ranger Hub (Optimization Biases)

| Subclass_ID | Role | Key Strength | Playstyle | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **GLOOM_STALK** | Alpha Striker | Dread Ambusher | Assassin | **GOD_TIER (Turn 1)** |
| **BEAST_MAST** | Action Economy | Companion | Tank/Hybrid | **S_TIER (Versatility)**|
| **SWARM_P8** | Utility / Zone | Gathered Swarm | Controller | **S_TIER (CC)** |
| **HUNTER** | AOE Blaster | Volley | Multi-Target | **A_TIER (Sustained)** |
| **DRAKE_P8** | Draconic Tank | Drake Companion | Elements | **A_TIER (Sustain)** |

---

## Matrix C: Scaling Registry (Companions & Swarms)

| Level | Companion_HP | Swarm_Die | Drake_Scaling | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **3** | 11 - 19 | 1d6 | Drake Core | [Wiki](https://bg3.wiki/wiki/Ranger) |
| **7** | 30 - 45 | 1d6 | Bond of Fangs | [Wiki](https://bg3.wiki/wiki/Ranger) |
| **11** | 60 - 90 | 1d8 | Perfection | [Wiki](https://bg3.wiki/wiki/Ranger) |

---

## Matrix G: Subclass Progression Registry (Granular)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **BEAST_MAST** | 3 | **PET_SUMMON** | ACTION | Summon Bear, Wolf, Boar, Spider, or Raven. |
| **BEAST_MAST** | 7 | **EXCPT_TRAIN** | PASSIVE | Companion can Dash, Disengage, Help as BA. |
| **BEAST_MAST** | 11| **BESTIAL_FURY** | PASSIVE | Companion gains Extra Attack (3x Total hits). |
| **GLOOM_STALK** | 3 | **DREAD_AMBUSH** | PASSIVE | +3m Speed, +1d8 dmg, +Special Attack on Turn 1.|
| **GLOOM_STALK** | 3 | **UMBRAL_SIGHT** | PASSIVE | Invisibility to creatures using Darkvision. |
| **GLOOM_STALK** | 7 | **IRON_MIND** | PASSIVE | Proficiency in WIS and INT Saving Throws. |
| **SWARM_P8** | 3 | **GATH_SWARM** | PASSIVE | Trigger Dmg, Push (4.5m), or Move (1.5m) on hit.|
| **SWARM_P8** | 7 | **WRITH_TIDE** | BONUS | Gain Hover Fly (60ft) for 1 minute. |
| **HUNTER** | 3 | **HUNTER_PREY** | SELECT | Colossus Slayer, Giant Killer, or Horde Breaker.|
| **HUNTER** | 11| **MULTIATTACK** | ACTION | Whirlwind (Melee) or Volley (Ranged) AOE. |

---

## Matrix E: Selection Pool Matrix (Full Forensic)

| Pool_ID | Choice_ID | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- |
| **FAV_ENEMY** | Bounty Hunter | **S** | Adv on Ensnaring Strike; Best for Archery CC. |
| **FAV_ENEMY** | Ranger Knight | **S** | Heavy Armor access; Mandatory for STR Rangers. |
| **FAV_ENEMY** | Keeper of Veil | **A** | Protection from Evil/Good; Strong defensive. |
| **NAT_EXPL** | Beast Tamer | **S** | Free Find Familiar (Action Economy soak). |
| **NAT_EXPL** | Urban Tracker | **S** | Sleight of Hand proficiency; Rogue substitute. |
| **NAT_EXPL** | Wasteland: Fire| **S** | Fire Resistance; Most common damage type. |
| **NAT_EXPL** | Wasteland: Pois| **A** | Poison Resistance; Critical for Act 1/2. |
| **STYLE** | Archery | **S** | +2 to Ranged Attacks; Mathematically dominant. |
| **STYLE** | Defense | **A** | +1 AC; Consistent value. |
| **H_PREY** | Colossus Slayer| **S** | +1d8 DMG vs non-full HP targets; Reliable. |
| **H_PREY** | Horde Breaker | **A** | Free attack on adjacent enemies; Clear power. |
| **H_PREY** | Giant Killer | **B** | Reaction attack vs Large enemies; Niche. |
| **H_DEFENSE**| Multi-Atk Def | **S** | +4 AC after being hit once; Best for melee tanks. |
| **H_DEFENSE**| Steel Will | **A** | Advantage vs Frightened; Strong late-game. |
| **H_DEFENSE**| Escape Horde | **B** | Disadv on enemy OA; Good for repositioning. |
| **H_ATTACK** | Volley (Range) | **S** | Ranged AOE; Primary late-game Ranger DPR. |
| **H_ATTACK** | Whirlwind (Mel)| **A** | Melee AOE; Strong for STR Rangers. |

---

## Matrix F: Build Synergy Biases (Agent-Logic)

| Synergy_ID | Component_A | Component_B | Logic_Goal |
| :--- | :--- | :--- | :--- |
| **TITANSTRING** | Titanstring Bow | STR Elixirs | Add STR mod to Ranged damage. |
| **DREAD_ASSASSIN**| Gloom Stalker 5 | Thief Rogue 4 | Infinite BA + 3-Attack Alpha Strike. |
| **SPIKE_ZONE** | Spike Growth | Swarm Push | Push enemies back into spikes repeatedly. |

### [TACTICAL] Natural Explorer Resistance Tiers
- **Act 1-2**: Prioritize **POISON** resistance (Goblins, Spiders, Shadow-Cursed Lands).
- **Act 3**: Prioritize **FIRE** resistance (Steel Watch, Fireballs, Dragons).

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Companion Dash Utility**: Companions can Dash as a Bonus Action (P8), allowing them to reposition and still use their primary Action for Multi-Attack or Special strikes.
> - **Resistance Strategy**: In Act 1-2, prioritize **Poison** resistance. Scale to **Fire** resistance for Act 3 Steel Watch encounters.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "RANGER_V13.2",
  "manifest_ref": "vanguard_manifest.json#RANGER",
  "patch_baseline": "8_HOTFIX36",
  "scaling_formulas": {
    "companion_ac": "Base_AC + Proficiency_Bonus",
    "companion_hit": "Base_Hit + Proficiency_Bonus",
    "companion_hp": "Level_Scaling_Table"
  },
  "companion_stats_lv11": {
    "dire_wolf": {"STR": 17, "DEX": 15, "CON": 15, "AC": 18, "HP": 84, "PB": 4},
    "bear": {"STR": 19, "DEX": 10, "CON": 16, "AC": 19, "HP": 99, "PB": 4},
    "giant_spider": {"STR": 14, "DEX": 16, "CON": 12, "AC": 17, "HP": 72, "PB": 4},
    "raven": {"STR": 6, "DEX": 16, "CON": 10, "AC": 16, "HP": 54, "PB": 4},
    "drake_p8": {"STR": 16, "DEX": 14, "CON": 14, "AC": 18, "HP": 80, "Dmg": "1d6+PB"}
  },
  "building_priorities": {
    "swarm_options_weight": {"Damage": 0.3, "Push": 0.6, "Move": 0.1},
    "favored_enemy_ranking": ["Bounty_Hunter", "Ranger_Knight", "Keeper_Veil"]
  }
}
```



