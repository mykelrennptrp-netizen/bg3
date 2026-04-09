---
id: CLASS_SORCERER
name: Sorcerer
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Sorcerer
primary_stat: CHA
secondary_stat: CON
tertiary_stat: DEX
hp_base: 6
hp_scaling: 4
armor_prof: NONE
weapon_prof: [DAGGER, QUARTERSTAFF, LIGHT_XBOW]
saving_throws: [CON, CHA]
---

# ✨ Sorcerer: v13.2 High-Fidelity Standard (Patch 8)

This node governs the ultimate metamagic specialist. It has been forensically satiated with the Octa-Matrix Standard, including **Shadow Magic (P8)** and full draconic ancestry mapping.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Sorcerer Rules
> - **Metamagic (SSoT)**: Spend Sorcery Points to modify spells.
> - **Sorcery Points**: 1 point per level (starts at Lv 2). Bonus Action to convert Slots <-> Points.
> - **Twinned Spell Lock**: Can ONLY target spells that "cannot target more than one creature" (e.g., *Haste* yes, *Fireball* no).
> - **Quickened Spell (P8)**: Cast spell as Bonus Action for 3 SP. **Honour Mode Lock**: Cannot cast two Level 1+ spells in the same turn (Cantrip + Spell only).
> - **Greater Invisibility (P8)**: In **Honour Mode**, the Stealth checks to maintain invisibility become **progressively harder** with each success.

---

## Matrix A: Core Class Progression (Lv 1-12)

| Lvl | Feature_ID | Type | Cost | Description |
| :--- | :--- | :--- | :--- | :--- |
| **1** | BLOODLINE | SELECT | - | Draconic, Storm, Shadow, or Wild Magic. |
| **2** | SORC_POINTS | RESOURCE | - | Use for Metamagic or Slot Creation. |
| **2** | METAMAGIC_1 | SELECT | - | Select 2 Metamagic options. |
| **3** | METAMAGIC_2 | SELECT | - | Select 1 additional Metamagic option. |
| **5** | SPELL_UPGRADE | PASSIVE | - | Level 3 Spell slots unlocked (Haste/Fireball). |
| **10** | METAMAGIC_3 | SELECT | - | Select final Metamagic option. |
| **11** | BLOODLINE_11 | PASSIVE | - | Final subclass feature (e.g., Flight, Shadow Walk).|

---

## Matrix B: Sorcerer Hub (Optimization Biases)

| Subclass_ID | Role | Key Strength | Playstyle | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **DRACONIC** | Blaster / Tank | 13 AC + HP | Sustained DPR | **GOD_TIER (Fire/Ice)**|
| **STORM** | Mobility God | BA Flying | AOE / Control | **S_TIER (Lightning)** |
| **SHADOW_P8** | Infiltrator | Shadow Hound | CC / Darkness | **S_TIER (Control)** |
| **WILD_MAGIC** | Chaos Mage | Tides of Chaos | RNG Burst | **A_TIER (Support)** |

---

## Matrix C: Scaling Registry (Sorcery Points)

| Level | Sorcery_Points | Slot_Creation | Metamagic_Cap | wiki_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **2** | 2 | Lv 1 | 2 Choices | [Wiki](https://bg3.wiki/wiki/Sorcerer) |
| **6** | 6 | Lv 3 | 3 Choices | [Wiki](https://bg3.wiki/wiki/Sorcerer) |
| **12** | 12 | Lv 5 | 4 Choices | [Wiki](https://bg3.wiki/wiki/Sorcerer) |

---

## Matrix G: Subclass Progression Registry (Granular)

| Subclass | Lvl | Gain_ID | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| **DRACONIC** | 1 | **DRAC_RESIL** | PASSIVE | AC 13 (unarmored) + 1 HP per level. |
| **DRACONIC** | 6 | **ELEM_AFFIN** | PASSIVE | Add CHA mod to dmg of Bloodline element. |
| **DRACONIC** | 11| **DRAC_WINGS** | PASSIVE | Permanent Fly speed (No cost). |
| **STORM** | 1 | **TEMP_MAGIC** | BONUS | Fly 9m after casting leveled spell (No OA). |
| **STORM** | 6 | **HEART_STORM** | PASSIVE | Deal [Lv/2] Dmg to enemies when casting elem.|
| **STORM** | 11| **STORM_FURY** | REACT | Deal [Lv] Lightning to target that hits you. |
| **SHADOW_P8** | 1 | **STREN_GRAVE**| PASSIVE | Drop to 1 HP instead of 0 once per LR. |
| **SHADOW_P8** | 6 | **HOUND_OMEN** | ACTION | Summon Hound; Target has Disadv on saves. |
| **SHADOW_P8** | 11| **SHADOW_WALK**| BONUS | Teleport 18m if in Dim Light or Darkness. |
| **WILD_MAG** | 1 | **TIDES_CHAOS**| ACTION | Gain Adv on next roll; Surge probability up. |
| **WILD_MAG** | 6 | **BEND_LUCK** | REACT | Use 2 SP to add/subtract 1d4 from target roll.|
| **WILD_MAG** | 11| **CONTR_CHAOS**| PASSIVE | Cause a surge on an enemy's spellcast. |

---

## Matrix E: Selection Pool Matrix (Full Forensic Pools)

| Pool_ID | Choice_ID | Tier | Optimization Logic |
| :--- | :--- | :--- | :--- |
| **METAMAGIC** | **Twinned** | **S** | Buff 2 allies (Haste) or hit 2 targets (Hold). |
| **METAMAGIC** | **Quickened** | **S** | Cast as Bonus Action; Burst king. |
| **METAMAGIC** | **Heightened** | **S** | Force Disadv on saves; Essential for high-DC CC.|
| **METAMAGIC** | **Distant** | **B** | Increase range by 50%; Good for Rapiers/Melee. |
| **METAMAGIC** | **Extended** | **B** | Double duration of buffs (e.g., 20-turn Haste).|
| **METAMAGIC** | **Subtle** | **C** | Cast while Silenced; Niche social/anti-mage. |
| **METAMAGIC** | **Careful** | **C** | Allies automatically succeed saves (AOE safety). |
| **DRAC_ANCEST**| **Red (Fire)** | **S** | Burning Hands; Best damage element in BG3. |
| **DRAC_ANCEST**| **Blue (Light)** | **S** | Witch Bolt; High synergy with wet targets. |
| **DRAC_ANCEST**| **White (Cold)** | **A** | Armour of Agathys; Essential for tank setups. |
| **DRAC_ANCEST**| **Gold (Fire)** | **A** | Disguise Self; Social flexibility + Fire dmg. |
| **DRAC_ANCEST**| **Brass (Fire)** | **B** | Sleep; Strong early game control. |
| **DRAC_ANCEST**| **Silver (Cold)** | **B** | Feather Fall; Utility focus. |
| **DRAC_ANCEST**| **Bronze (Light)**| **B** | Fog Cloud; Vision denial / Infiltration. |
| **DRAC_ANCEST**| **Copper (Acid)** | **C** | Tasha's Laughter; Single target CC. |
| **DRAC_ANCEST**| **Black (Acid)** | **C** | Grease; Terrain control. |
| **DRAC_ANCEST**| **Green (Pois)** | **C** | Ray of Sickness; Least effective element. |
| **SPELL_S** | **Haste** | **S** | Premier action-economy multiplier. |
| **SPELL_S** | **Fireball** | **S** | Gold-standard for AOE damage. |
| **SPELL_S** | **Hold Person/Mo**| **S** | Autocritic control states. |
| **SPELL_S** | **Counterspell**| **S** | Action-economy denial vs magic users. |
| **SPELL_S** | **Shield** | **A** | Critical defensive reaction utility. |
| **SPELL_S** | **Magic Missile**| **A** | Guaranteed damage; Item-synergy king. |
| **SPELL_S** | **Misty Step** | **A** | Essential combat mobility. |

---

## Matrix F: Build Synergy Biases (Agent-Logic)

| Synergy_ID | Component_A | Component_B | Logic_Goal |
| :--- | :--- | :--- | :--- |
| **SORLOCK_GEN** | Eldritch Blast | Quickened Spell | 3-beam x 2 spam with Potent Robe. |
| **TWIN_LOCK** | Twinned Spell | Single Target | Prevent hallucinating "Twinned Fireball." |
| **SHADOW_STEP** | Shadow Walk | Darkness Spell | Create teleport anchor points anywhere. |
| **ICE_QUEEN** | White Draconic | Agathys + Abjur | Reflect damage while remaining un-hittable. |

---

---

> [!TIP]
> ### Agent-Optimization Logic
> - **Metamagic Selection**: `Twinned Spell` is the absolute priority for early-game buffs (Haste), while `Heightened Spell` becomes mandatory at high levels to overcome Boss Legendary Resistances.
> - **Shadow Walker Strategy**: Shadow Sorcerers should cast `Darkness` to create teleport anchors, effectively granting ~18m of free vertical/horizontal movement as a Bonus Action.

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "class_id": "SORCERER_V13.2",
  "manifest_ref": "vanguard_manifest.json#SORCERER",
  "patch_baseline": "8_HOTFIX36",
  "metamagic_costs": {
    "twinned": "Spell_Level",
    "quickened": 3,
    "heightened": 3,
    "distant": 1,
    "subtle": 1,
    "extended": 1,
    "careful": 1
  },
  "shadow_magic_p8": {
    "shadow_walk_light_threshold": "DIM_LIGHT_OR_LOWER",
    "hound_disadvantage_radius": "MELEE_RANGE"
  },
  "building_priorities": {
    "draconic_ac_override": 13,
    "sorcery_point_conversion": "1_POINT_PER_LVL",
    "honour_mode_quickened_limit": "ONE_LEVELED_SPELL_PER_TURN",
    "honour_mode_invis_escalation": true
  }
}
```


