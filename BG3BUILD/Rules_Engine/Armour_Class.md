---
id: RULES_ARMOUR_CLASS
name: Armour Class Rules Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Armour_Class
logic_type: DEFENSIVE_CALCULATION
---

# 🛡️ Armour Class: v13.2 High-Fidelity Standard (Patch 8)

This node governs the defensive threshold of all characters. It has been forensically satiated with the Octa-Matrix Standard, including **Unarmoured Defense** and **Shield** stacking logic.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core AC Rules
> - **Base AC (SSoT)**: 10 + DEX Mod (unless wearing Armor).
> - **Light Armour**: Full DEX Mod applied.
> - **Medium Armour**: DEX Mod capped at **+2** (unless *Medium Armour Master* feat or *Exotic Material* property).
> - **Heavy Armour**: NO DEX Mod applied. Bases: 14 (Ring Mail) up to 18 (Plate).
> - **Shields**: Standard gain is **+2 AC**.

---

## 📊 Matrix A: Formula Overrides (Build Anchors)

| Source | Formula | Impact | wiki_Anchor |
| :--- | :--- | :--- | :--- |
| **CLOTHING** | 10 + DEX Mod | Standard caster/rogue baseline. | [Wiki](https://bg3.wiki/wiki/Clothing) |
| **MAGE_ARMOUR** | 13 + DEX Mod | Level 1 Spell; Essential for Wizards. | [Wiki](https://bg3.wiki/wiki/Mage_Armour) |
| **BARB_UA_DEF** | 10 + DEX + CON | Barbarian only; Shields allowed. | [Wiki](https://bg3.wiki/wiki/Unarmoured_Defence_(Barbarian))|
| **MONK_UA_DEF** | 10 + DEX + WIS | Monk only; NO Shields allowed. | [Wiki](https://bg3.wiki/wiki/Unarmoured_Defence_(Monk)) |
| **DRACONIC_AC** | 13 + DEX Mod | Sorcerer (Draconic) base AC. | [Wiki](https://bg3.wiki/wiki/Draconic_Resilience) |
| **BARKSKIN** | Min AC 16 | Fixed floor; Ignores base AC < 16. | [Wiki](https://bg3.wiki/wiki/Barkskin) |
| **SHIELD_SOF** | +2 AC (Buff) | Concentrated bonus; Stacks with armor. | [Wiki](https://bg3.wiki/wiki/Shield_of_Faith) |
| **SHIELD_REAC** | +5 AC (Reac) | Until start of next turn. | [Wiki](https://bg3.wiki/wiki/Shield_(Spell)) |
| **DUAL_WIELDER**| +1 AC (Pass) | While wielding two melee weapons. | [Wiki](https://bg3.wiki/wiki/Dual_Wielder) |
| **DEFENSE_STY**| +1 AC (Pass) | While wearing armor (Fighter/Paladin). | [Wiki](https://bg3.wiki/wiki/Fighting_Style:_Defence) |
| **WARD_BOND** | +1 AC (Pass) | Resistance +1 AC (Cleric spell). | [Wiki](https://bg3.wiki/wiki/Warding_Bond) |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "ARMOUR_CLASS_V13.2",
  "manifest_ref": "vanguard_manifest.json#ENGINE",
  "patch_baseline": "8_HOTFIX36",
  "ac_caps": {
    "medium_armour_dex_limit": 2,
    "heavy_armour_dex_limit": 0,
    "shield_standard_bonus": 2
  },
  "unarmoured_logic": {
    "monk": {"stat_1": "DEX", "stat_2": "WIS", "shield_penalty": true},
    "barbarian": {"stat_1": "DEX", "stat_2": "CON", "shield_penalty": false}
  }
}
```
