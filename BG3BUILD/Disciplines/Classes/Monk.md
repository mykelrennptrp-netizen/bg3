---
id: CLASS_MONK
name: Monk
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Monk
primary_stat: DEX
secondary_stat: WIS
tertiary_stat: CON
hp_base: 8
hp_scaling: 5
armor_prof: NONE
weapon_prof: [SIMPLE, SHORTSWORDS]
saving_throws: [STR, DEX]
---

# 🥋 Monk: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate mobile combatant. It has been forensically satiated with the Octa-Matrix Standard, including **Way of the Drunken Master (P8)** and full Elemental Discipline selection pools.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Monk Rules
> - **Unarmoured Defence**: AC = 10 + DEX + WIS. Does not stack with other Unarmoured Defence features (e.g., Barbarian).
> - **Shadow Strike (P8)**: Damage roll doubling bug has been **FIXED**. Standard 3d8 Psychic scaling applied.
> - **Step of the Wind (P8)**: Jumping no longer requires a Bonus Action if you have used **Step of the Wind: Dash**.
> - **Martial Arts**: Bonus Action Unarmed Strike is available after attacking with a Monk Weapon or Unarmed Strike.

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | UNARMORED_DEF | PASSIVE | - | AC = 10 + DEX + WIS. |
| **1** | MARTIAL_ARTS | PASSIVE | - | Use DEX for Monk Weapons; BA Unarmed Strike. |
| **2** | KI_POINTS | RESOURCE| - | Gain Ki points (1 per level). |
| **2** | UNARMORED_MVMT| PASSIVE | - | Movement speed increases (+3m to +6m). |
| **3** | DEFLECT_MISSL | REACT | - | Reduce ranged weapon damage by 1d10 + DEX + Lvl. |
| **4** | SLOW_FALL | REACT | - | Halve falling damage. |
| **5** | EXTRA_ATTACK | PASSIVE | - | Attack twice per Action. |
| **5** | STUNNING_STRK | ACTION | 1_KI | Chance to Stun target (CON save). |
| **7** | STILLNESS_MIND| PASSIVE | - | Automatically end Charmed or Frightened. |
| **7** | EVASION | PASSIVE | - | Half damage on failed DEX save; Zero on success. |
| **10** | PURITY_BODY | PASSIVE | - | Immune to Poison damage and the Poisoned condition.|

---

## Matrix B: Monk Hub (Building Biases)

| Subclass_ID | Role | Key Strength | Playstyle | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **OPEN_HAND** | Raw DPR King | Manifestations | Aggressive | **GOD_TIER (DPR)** |
| **DRUNKEN (P8)**| Mobile Tank | Intoxication | Brawler | **S_TIER (AEO/Mobility)**|
| **SHADOW** | Stealth / Utly | Teleportation | Assassin | **S_TIER (Infiltration)**|
| **ELEMENTS** | Caster / CC | Disciplines | Hybrid | **A_TIER (Versatility)** |

---

## Matrix C: Scaling Registry (Resources)

| Level | Ki_Points | Martial_Arts_Die | Unarm_Move | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **2** | 2 | 1d4 | +3m | [Wiki](https://bg3.wiki/wiki/Monk) |
| **3** | 3 | 1d6 | +3m | [Wiki](https://bg3.wiki/wiki/Monk) |
| **6** | 6 | 1d6 | +4.5m | [Wiki](https://bg3.wiki/wiki/Monk) |
| **9** | 9 | 1d8 | +4.5m | [Wiki](https://bg3.wiki/wiki/Monk) |
| **12** | 12 | 1d8 | +6m | [Wiki](https://bg3.wiki/wiki/Monk) |

---

## Matrix G: Subclass Progression Registry (Granular)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **OPEN_HAND** | 3 | **OH_TECHNIQUE** | PASSIVE | Flurry can Topple, Push, or Stagger targets. |
| **OPEN_HAND** | 6 | **MANIFESTATION**| PASSIVE | Add 1d4+WIS Necrotic, Radiant, or Psychic dmg. |
| **OPEN_HAND** | 6 | **WHOLENESS** | ACTION | Heal + Recover Ki + Gain extra Bonus Action. |
| **OPEN_HAND** | 9 | **KI_RESONATE** | ACTION | Punch target to explode them later (AOE Force). |
| **OPEN_HAND** | 11| **TRANQUILITY** | PASSIVE | Gain Sanctuary after a Long Rest. |
| **DRUNKEN_P8** | 3 | **DRUNK_TECH** | PASSIVE | Gain Disengage + 3m Speed when using Flurry. |
| **DRUNKEN_P8** | 3 | **DRUNK_MAST** | BONUS | Drink Alcohol to gain Temp HP + Drunk state. |
| **DRUNKEN_P8** | 6 | **TIPSY_SWAY** | PASSIVE | Leap to feet for 3m speed; Redirect missed hits. |
| **DRUNKEN_P8** | 11| **DRUNK_FRENZY** | ACTION | Flurry targets ALL neighbors (AOE Burst). |
| **SHADOW** | 3 | **SHADOW_ARTS** | KI | Cast Darkness, Silence, Pass Trace, Darkvision. |
| **SHADOW** | 6 | **SHADOW_STEP** | BONUS | Teleport from shadow to shadow (Adv on next hit).|
| **SHADOW** | 11| **SHADOW_STRK** | ACTION | Teleport 18m + 3d8 Psychic damage (3 Ki). |
| **ELEMENTS** | 3 | **DISCIPLINES** | RESOURCE| Select 3 Elemental Disciplines. |
| **ELEMENTS** | 6 | **HARMONY** | ACTION | Recover half Ki Outside of combat. |
| **ELEMENTS** | 11| **ADV_DISCIP** | CHOICE | Select high-level Elemental Disciplines. |

---

## Matrix E: Selection Pool Matrix (Full Forensic Pools)

| Pool_ID | Choice_ID | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- |
| **ELEM_DISC** | Fangs of Fire Snake| **S** | Unarmed Dmg + 6m Reach + 1d10 Fire. |
| **ELEM_DISC** | Water Whip | **S** | 25m Pull + 3d10 Bludgeoning + Prone. |
| **ELEM_DISC** | Fist of Unbroken Air| **S** | 9m Push + 3d10 Bludgeoning + Prone. |
| **ELEM_DISC** | Flames of Phoenix | **A** | Fireball equivalent (Lv 9). |
| **ELEM_DISC** | Gong of the Summit | **A** | Shatter equivalent (Lv 6). |
| **ELEM_DISC** | Clench of North Wind| **A** | Hold Person equivalent (Lv 6). |
| **ELEM_DISC** | Fist of 4 Thunders | **B** | Thunderwave equivalent. |
| **ELEM_DISC** | Rush of Gale Spirits| **B** | Gust of Wind equivalent. |
| **ELEM_DISC** | Shaping of the Ice | **B** | Create Ice Surface / Ice Knife logic. |
| **ELEM_DISC** | Ride the Wind | **B** | Fly equivalent (Lv 9). |
| **ELEM_DISC** | Mist Stance | **B** | Gaseous Form equivalent (Lv 9). |
| **ELEM_DISC** | Embrace of Earth | **C** | Entangle equivalent. |
| **ELEM_DISC** | Sphere Elem Energy | **C** | Chromatic Orb equivalent. |
| **SHADOW_ART** | Darkness | **S** | Tactical AOE Blindness. |
| **SHADOW_ART** | Pass w/o Trace | **S** | +10 Stealth (Guaranteed Surprise). |
| **SHADOW_ART** | Silence | **A** | Prevent enemy casting in shadow zones. |
| **SHADOW_ART** | Darkvision | **B** | Utility for races without innate vision. |
| **OH_TECH** | Topple (Prone) | **S** | Melee Advantage multiplier. |
| **OH_TECH** | Stagger (React) | **A** | Deny enemy Reactions. |
| **OH_TECH** | Push (9m) | **A** | Forced movement for hazard kills. |

---

## Matrix F: Build Synergy Biases (Agent-Logic)

| Synergy_ID | Component_A | Component_B | Logic_Goal |
| :--- | :--- | :--- | :--- |
| **TB_MONK_STR** | Tavern Brawler | STR Elixirs | Infinite accuracy + Massive static damage. |
| **DRUNKEN_BEAR**| Drunken Master 9 | Barbarian 3 | Massive Resistances + AOE Intoxicated Frenzy. |
| **SHADOW_SNEAK**| Shadow Monk 6 | Thief Rogue 4 | Bonus Action Teleport + 2nd BA for Invisibility. |
| **RADIO_STUN** | Open Hand (Rad) | Luminous Armor | Inflict Radiating Orb on every punch. |

---

> [!TIP]
> ### Agent-Optimization Logic
> - **TB Scaling**: Tavern Brawler + STR Elixirs is the absolute DPR ceiling for Monks. Prioritize `WIS` for Stunning Strike DC only after maximizing attack accuracy.
> - **Drunken Mastery**: Drunken Masters must maintain 100% uptime on the `Drunk` state to leverage constant Temp HP and Redirect Attack reactions.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "MONK_V13.2",
  "manifest_ref": "vanguard_manifest.json#MONK",
  "patch_baseline": "8_HOTFIX36",
  "building_priorities": {
    "stat_weight": {"DEX": 1.0, "WIS": 0.8, "CON": 0.6, "STR": 0.4},
    "multiclass_dips": {
      "Rogue_Thief": "Second_Bonus_Action_Priority",
      "Barbarian_3": "Resistance_Drunken_Bear"
    },
    "feat_ranking": ["Tavern_Brawler", "Alert", "Mobile", "Ability_Improvement"]
  },
  "subclass_logic": {
    "open_hand_manifestation": "1d4 + WIS_MOD",
    "drunken_master_p8": {"temp_hp_drink": true, "redirect_attack_reaction": true},
    "shadow_strike_p8": {"psychic_dmg": "3d8", "is_fixed": true}
  }
}
```


