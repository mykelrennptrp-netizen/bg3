---
id: EQUIPMENT_SYNERGY
name: Synergy Item Database (Final Arsenal)
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Equipment
forensic_status: HARDENED
---

# Equipment Synergy: v13.2 Forensic Satiation

This node is the Single Source of Truth (SSoT) for high-optimization item interactions. It has been forensically hardened against [appendices.txt](file:///c:/Users/REHAB/Desktop/BG3_Antigravity/appendices.txt) to eliminate all data truncation.

## ⚙️ Core Synergy Logic (P8 Hardware)
- **Arcane Acuity (MAX 10)**: +1 Spell DC/Attack roll per stack. Decays -2 per turn.
- **Reverberation (MAX 5)**: -1 STR/DEX/CON saves per stack. At 5 stacks: 1d4 Thunder + Prone (DEX Save DC 10).
- **Radiating Orb (MAX 10)**: -1 Attack roll per stack. Decays -2 per turn.
- **Vulnerability Logic**: Bhaalist Armour (Piercing) and Arsonist's Oil (Fire) provide permanent/conditional 2x damage multipliers.

---

## Matrix A: Status Effect Sets (Condition Meta)

| Item_ID | Slot | Effect | Synergy_ID | Logic_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **LUMINOUS_ARM** | Chest | AoE Rad-Orb (3m) on Radiant damage. | RAD_ORB | [Appendices:L1377] |
| **CORUSC_RING** | Ring | Rad-Orb (2 turns) on Spell Damage. | RAD_ORB | [Appendices:2259] |
| **LUMIN_GLOVES** | Gloves | Rad-Orb (2 turns) on Radiant damage. | RAD_ORB | [Appendices:1856] |
| **STORMY_BOOTS** | Boots | Reverberation (2 turns) on Condition Apply. | REVERB | [Appendices:1585] |
| **BELLI_GLOVES** | Gloves | Reverberation (2 turns) on Thunder/Light/Rad. | REVERB | [Appendices:1781] |
| **THUND_CLOAK** | Cloak | Daze reverberating creature when hit. | REVERB | [Appendices:1691] |

---

## Matrix B: Resource & Stat Engines

| Item_ID | Slot | Effect | Optimization_Role | Logic_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **FIRE_ACU_HAT** | Head | Gain Arcane Acuity on Fire damage. | ACUITY_ENGINE | [Appendices:2009] |
| **SCOUND_BAND** | Ring | BA Illusion/Enchant after Weapon hit. | ACTION_ECONOMY | [Appendices:2246] |
| **HILL_GIANT_GL** | Gloves | Set Strength to **23**. | ATTRIBUTE_FIX | [Appendices:1752] |
| **DEX_GLOVES** | Gloves | Set Dexterity to **18**. | ATTRIBUTE_FIX | [Appendices:1789] |
| **HEALTH_AMUL** | Amulet | Set Constitution to **23** + CON Adv. | ATTRIBUTE_FIX | [Appendices:2122] |
| **RISKY_RING** | Ring | Advantage on Attacks / Disadv on Saves. | PERMA_ADV | [Appendices:2347] |

---

## Matrix C: BiS Weapon Registry (Strategic Staples)

| Weapon_ID | Type | Effect | Meta_Role | Logic_Anchor |
| :--- | :--- | :--- | :--- | :--- |
| **MARKOHESHKIR** | Staff | Kereska's Favor (Buff) + Arcane Battery. | CASTER_BIS | [Appendices:690] |
| **NYRULNA** | Trident | AOE Thunder Thrown + Mobility + Homing. | THROWER_BIS | [Appendices:981] |
| **BHAAL_ARMOUR** | Chest | Aura of Murder (Piercing Vuln @ 2m). | DPR_MULTIPLIER | [Appendices:1314] |
| **DWARVEN_THR** | Hammer | +2d8 vs Big targets; Homing (Dwarf). | THROWER_BIS | [Appendices:1006] |
| **PHALAR_ALUVE** | Sword | Shriek (1d4 Thunder Rider) / Sing. | BUFF_SUPPORT | [Appendices:964] |
| **POTENT_ROBE** | Robe | Add CHA to Cantrip Dmg + Temp HP. | ELDRITCH_BLAST | [Appendices:1245] |

---

## Matrix D: Alchemical Economy

| Item_ID | Type | Effect | Synergy_ID | Condition |
| :--- | :--- | :--- | :--- | :--- |
| **BLOODLUST_EL** | Elixir | +1 Action on Kill + 5 HP. | ACTION_ECON | Until Long Rest |
| **CLOUD_GIANT** | Elixir | Set Strength to **27**. | ATTRIB_GM | Until Long Rest |
| **SPEED_POTION** | Potion | **Haste** (Extra Action/AC/Saves). | ACTION_ECON | 3 Turns (Lethargy) |
| **ARSONIST_OIL** | Coating | Fire Resistance -> Vulnerability. | DPR_MULT | 10 Turns |

---

## 📦 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "vault_id": "EQUIPMENT_SYNERGY_V13_2",
  "patch_baseline": "8_HOTFIX36",
  "archetype_weights": {
    "fire_sorcerer": ["FIRE_ACU_HAT", "MARKOHESHKIR", "SCOUND_BAND"],
    "radiant_cleric": ["LUMINOUS_ARM", "CORUSC_RING", "STORMY_BOOTS"],
    "piercing_archer": ["BHAAL_ARMOUR", "RISKY_RING", "DEAD_SHOT"]
  },
  "proc_calibration": {
    "phalar_shriek": "evaluated_as_separate_damage_instance",
    "magic_missile_scaling": "procs_callous_glow_per_missile"
  }
}
```
