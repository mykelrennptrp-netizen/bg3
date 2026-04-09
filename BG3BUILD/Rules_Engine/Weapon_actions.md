---
id: WEAPON_ACTIONS
name: Weapon Action Logic Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
category: RULES_ENGINE
forensic_status: HARDENED
---

# Weapon Action Matrix: v13.2 Hardened

This node governs the tactical logic for weapon-specific abilities. All actions are grounded in `bg3.wiki` and synchronized with the [appendices.txt](file:///c:/Users/REHAB/Desktop/BG3_Antigravity/appendices.txt) forensic source.

## ⚙️ Core Engine Logic
- **Requirement**: Must be proficient with the weapon and have it equipped in the **Main Hand**.
- **Economy**: Default is **Once Per Short Rest**. Swapping weapons does not reset the cooldown if the same action type was already used.
- **Difficulty Class (DC)**: `10 + max(STR_MOD, DEX_MOD) + Item_Enchantment_Bonus`.

## 🗡️ Special Attacks Matrix

| Action_ID | Cost | Save | Effect | Duration | Categories |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **BACKBREAKER** | Action | STR | Inflict **Prone**. | 2 Turns | Hammers, Mauls, Warhammers |
| **BRACE** | 6m Move | N/A | Roll weapon damage twice (take better). | End of Turn | Polearms, Pikes, Bows |
| **CLEAVE** | Action | N/A | 50% Damage to 3 targets in 1.5m cone. | Instant | Greataxes, Greatswords, Halberds |
| **CONCUSSIVE** | Action | CON | Inflict **Dazed** (No Dex AC, No Reactions). | 2 Turns | Clubs, Maces, Flails, Morningstars |
| **FLOURISH** | BA | DEX | Inflict **Off-Balance** (Adv for attackers). | 2 Turns | Scimitars, Rapiers, Shortswords |
| **HAMSTRING** | Action | CON | Reduce Movement by 50%. | 2 Turns | Bows, Crossbows, Blades |
| **LACERATE** | Action | CON | Inflict **Bleeding** (2 dmg/turn, -CON Save). | 2 Turns | Axes, Swords, Glaives, Sickles |
| **PIERCING_STR** | Action | CON | Inflict **Gaping Wounds** (+2 Piercing Dmg). | 2 Turns | Daggers, Rapiers, Spears, Tridents |
| **POMMEL_STR** | BA | CON | 1d4 + Stat (Non-lethal) + **Dazed**. | 2 Turns | Longswords, Greatswords |
| **PREPARE** | 6m Move | N/A | Add **Strength Modifier twice** to damage. | End of Turn | Greataxes |
| **RUSH_ATTACK** | Action | STR | Charge 9m + **Off-Balance**. | 2 Turns | Longswords, Spears, Tridents |
| **TENACITY** | Reaction | N/A | On miss: Deal damage = STR modifier. | Instant | Mauls, Flails, Morningstars |
| **TOPPLE** | Action | DEX | Inflict **Prone**. | 1 Turn | Quarterstaves |
| **WEAK_GRIP** | Action | STR | Inflict **Weak Grip** (-Adv on Attacks). | 2 Turns | Flails, Rapiers, Warhammers |

---

## 📦 Layer 4: JSON Satiation Pod (Agent-Only)

```json
{
  "logic_root": "WEAPON_ACTIONS_V13_2",
  "mechanics": {
    "dc_formula": "10 + max(STR, DEX) + ItemBonus",
    "cooldown_standard": "SHORT_REST_1",
    "finesse_bypass": "Daggers use STR by default for Thrown range unless Dex is higher"
  },
  "tag_priority": {
    "CC": ["BACKBREAKER", "TOPPLE", "CONCUSSIVE"],
    "DEBUFF": ["LACERATE", "PIERCING_STR", "WEAK_GRIP"],
    "DPR_BOOST": ["BRACE", "PREPARE"]
  }
}
```
