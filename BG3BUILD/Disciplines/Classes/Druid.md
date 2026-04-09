---
id: CLASS_DRUID
name: Druid
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Druid
primary_stat: WIS
secondary_stat: CON
tertiary_stat: DEX
hp_base: 8
hp_scaling: 5
armor_prof: [LIGHT, MEDIUM, SHIELDS]
weapon_prof: [CLUB, DAGGER, JAVELIN, MACE, QUARTERSTAFF, SCIMITAR, SICKLE, SPEAR]
saving_throws: [INT, WIS]
---

# 🦌 Druid: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate shapeshifter. It has been forensically satiated with the Octa-Matrix Standard, including **Step 1: The Core & Specialist Circles**.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Druid Rules
> - **Tavern Brawler (P8)**: Now correctly works with Wild Shapes in **Honour Mode** (DPR parity).
> - **Myrmidon Proficiencies (P8)**: Character proficiencies now **MERGE** with the Myrmidon's, improving hit rates for multiclassed druids.
> - **Wild Strike + War Priest (P8)**: Martial extra attacks now stack with War Priest bonus attacks in Wild Shape.
> - **Grasping Vine (P8)**: Upcasted versions now cost a **BONUS ACTION** instead of an Action (Critical utility buff).
> - **Starry Form (P8)**: New transformation type that does not prevent spellcasting.

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | SPELLCASTING | PASSIVE | - | WIS-based preparation caster. |
| **2** | WILD_SHAPE | ACTION | 1_CHARGE | Transform into bestial forms. |
| **2** | CIRCLE_SELECT | SELECT | - | Select Druid Circle (Subclass). |
| **4** | WILD_SHAPE_IMP | PASSIVE | - | Gain new forms (Deep Rothe). |
| **5** | WILD_STRIKE | PASSIVE | - | Attack twice while in Wild Shape. |
| **6** | PRIMAL_STRIKE | PASSIVE | - | Wild Shape attacks count as **MAGICAL**. |
| **10** | IMPROVED_STRIKE | PASSIVE | - | Attack THREE times while in Wild Shape. |

---

## Matrix B: Circle Hub (Optimization Biases)

| Subclass_ID | Role | Transformation | Theme | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **MOON** | Main Tank / DPR | Combat Wild Shape | Beast Fury | **GOD_TIER (Sustain)** |
| **STARS (P8)** | Support / Blast | Starry Form | Celestial | **S_TIER (Versatility)**|
| **SPORES** | Gish / Necro | Symbiotic Entity | Fungal Decay | **S_TIER (Health Pool)**|
| **LAND** | Pure Caster | Natural Recovery | Elemental | **A_TIER (Endurance)** |

---

## Matrix C: Scaling Registry (Shapes & Spores)

| Level | Wild_Shape_Charges | WS_Max_HP (Bear/Owlbear) | Spore_Temp_HP (4*Lvl) | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **2** | 2 | 30 | 8 | [Wiki](https://bg3.wiki/wiki/Druid) |
| **4** | 2 | 39 / - | 16 | [Wiki](https://bg3.wiki/wiki/Druid) |
| **6** | 2 | 51 / 65 | 24 | [Wiki](https://bg3.wiki/wiki/Druid) |
| **8** | 2 | 63 / 84 | 32 | [Wiki](https://bg3.wiki/wiki/Druid) |
| **10** | 2 | 75 / 104 | 40 | [Wiki](https://bg3.wiki/wiki/Druid) |
| **12** | 2 | 87 / 124 | 48 | [Wiki](https://bg3.wiki/wiki/Druid) |

---

## Matrix G: Subclass Progression Registry (Granular - Batch 1)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **MOON** | 2 | **COMBAT_WS** | BONUS | Wild Shape uses Bonus Action. |
| **MOON** | 2 | **LUNAR_MEND** | BONUS | Expend spell slots to heal while transformed. |
| **MOON** | 2 | **BEAR_FORM** | WS | Gain high-HP Bear form. |
| **MOON** | 6 | **PRIME_STRIKE** | PASSIVE | WS attacks bypass non-magical resistance. |
| **MOON** | 10| **MYRMIDONS** | WS | Transform into Air/Earth/Fire/Water Myrmidons. |
| **STARS (P8)** | 2 | **STAR_MAP** | PASSIVE | Gain Guidance & Guiding Bolt (Free casts). |
| **STARS (P8)** | 2 | **STARRY_FORM** | BONUS | Choose Archer, Chalice, or Dragon form. |
| **STARS (P8)** | 6 | **COSMIC_OMEN** | REACT | Add 1d6 to rolls (Weal) or subtract (Woe). |
| **STARS (P8)** | 10| **TWINKLING** | PASSIVE | Starry Forms gain flight & increased damage. |
| **SPORES** | 2 | **HALO_SPORES** | REACT | 1d4 Necrotic damage whenever enemy gets close.|
| **SPORES** | 2 | **SYM_ENTITY** | ACTION | Gain Temp HP + d6 Necro on weapon attacks. |
| **SPORES** | 6 | **FUNGAL_INFEST**| ACTION | Raise dead as Fungal Zombies. |
| **SPORES** | 10| **SPREAD_SPORE** | BONUS | Create a Cloud of Spores (AOE Damage). |
| **LAND** | 2 | **NAT_RECOVER** | ACTION | Recover spell slots during a Short Rest. |
| **LAND** | 3 | **CIRCLE_SPELL** | CHOICE | Select Biome (Arctic, Coast, etc.) for spells. |
| **LAND** | 6 | **LAND_STRIDE** | PASSIVE | Ignore difficult terrain and plants. |
| **LAND** | 10| **NATURE_WARD** | PASSIVE | Immune to Poison, Disease, and Charmed/Frightened by fey/elementals. |

---

## Matrix E: Wild Shape Tier Matrix (Full Forensic Pool)

| Form_ID | Role | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- |
| **OWLBEAR** | Control / DPR | **S** | Crushing Flight = AOE Prone + High base HP. |
| **MYRMIDONS** | Elemental God | **S** | Fly + 3x Multi-attack + Weapon Prof Merging. |
| **PANTHER** | Stealth / Burst | **A** | Prowl Invisibility + Jugular Strike synergy. |
| **SABRETOOTH**| Shredder | **A** | Reduce enemy AC on hit + Passive Regen. |
| **DEEP ROTHE** | Force Breaker | **B** | Charge (Prone) + Magical Force Damage. |
| **SPIDER** | Crowd Control | **B** | Web (Ensnare) + Poison damage. |
| **DILOPHOSAUR**| Acid Tank | **B** | Corrosive Spit (-AC) + Pounce. |
| **WOLF** | Pack Support | **B** | Expose Throat (Crit) + Ally Advantage. |
| **RAVEN** | Scout / Flight | **C** | High mobility; Beak Attack (Blind). |
| **BADGER** | Burrower | **C** | Burrow (Prone) + Multiattack. |
| **CAT** | Stealth Scout | **D** | Sneak into tiny gaps; Inconspicuous. |

---

## Matrix E: Land Biome Spell Matrix (Compact)

| Biome | Lv 3 Spells | Lv 5 Spells | Lv 7 Spells | Lv 9 Spells |
| :--- | :--- | :--- | :--- | :--- |
| **ARCTIC** | Hold Pers, Spike G | Sleet St, Haste | Confusion, Ice St | Cone Cold, Contagion |
| **COAST** | Mirror Im, Misty St | Call Light, Sleet St | Confusion, G. Invis | Cloudkill, Conj Elem |
| **DESERT** | Blur, Silence | Prot Energy, Hypnotic| Blight, Wall Fire | Insect Pl, Wall Stone|
| **FOREST** | Barkskin, Hold Pers | Call Light, Plant Gr | Confusion, Grasp Vine| Contagion, Insect Pl |
| **GRASS** | Invis, Pass Trace | Daylight, Haste | Confusion, Freedom M | Cloudkill, Insect Pl |
| **MOUNT** | Mirror Im, Spike G | Call Light, Light B | Blight, Ice St | Cloudkill, Wall Stone|
| **SWAMP** | Acid Arr, Darkness | Gaseous F, Stink Cl | Blight, Grasp Vine | Cloudkill, Insect Pl |
| **UDARK** | Blindness, Misty St | Gaseous F, Stink Cl | Blight, G. Invis | Cloudkill, Insect Pl |

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Myrmidon Merging**: Prioritize multiclassing with classes that provide relevant weapon proficiencies (e.g., Fighter) to enhance Myrmidon attack rolls via the P8 merging mechanic.
> - **Starry Form Priority**: `Dragon Form` is the mandatory selection for concentration-heavy setups to ensure a minimum roll of 10 on all saves.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "DRUID_V13.2",
  "manifest_ref": "vanguard_manifest.json#DRUID",
  "patch_baseline": "8_HOTFIX36",
  "building_priorities": {
    "stat_weight": {"WIS": 1.0, "CON": 0.8, "DEX": 0.6},
    "multiclass_dips": {
      "Fighter_1": "Constitution_Saving_Throw_Start",
      "Cleric_Life": "Heavy_Armor_Healing_Synergy"
    },
    "feat_ranking": ["Tavern_Brawler", "War_Caster", "Alert", "Sentinel"]
  },
  "wild_shape_stats": {
    "bear": {"STR": 19, "DEX": 10, "CON": 16},
    "owlbear": {"STR": 20, "DEX": 12, "CON": 17},
    "panther": {"STR": 14, "DEX": 15, "CON": 12},
    "myrmidons": {"STR": 18, "DEX": 14, "CON": 16}
  },
  "subclass_logic": {
    "stars_dragon_conc": "MIN_ROLL_10",
    "spores_symbiotic_hp": "4_PER_LVL",
    "moon_lunar_mend": "SLOT_BASED_HEAL",
    "grasping_vine_ba": "UPCAST_ONLY"
  }
}
```


