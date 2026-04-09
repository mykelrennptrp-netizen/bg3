---
id: LIBRARY_CONSUMABLES
name: Consumables & Elixir Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Consumables
logic_type: ATTRIBUTE_OVERRIDE_MAPPING
---

# 🍶 Consumables: v13.2 High-Fidelity Standard (Patch 8)

This node governs high-impact elixirs and potions that anchor build architecture. It has been forensically satiated with the **Long-Rest Elixir Matrix** for Gemini Pro optimization.

> [!IMPORTANT]
> ### [WIKI_LOCK] Elixir Rules
> - **Long-Rest Duration**: Elixirs last until the next Long Rest.
> - **Mutual Exclusivity**: Drinking a new elixir immediately replaces the current one.
> - **Attribute Overrides**: Strength Elixirs set the attribute to a fixed value (21 or 27), overwriting the base stat regardless of its current value.

---

## 📊 Matrix A: Long-Rest Elixir Mastery (Build Anchors)

| Elixir_ID | Mechanical Effect | Primary Build Synergy | Optimization_Cap |
| :--- | :--- | :--- | :--- |
| **CLOUD_GIANT** | Sets **STR to 27**. | Tavern Brawler / GWM Martials. | **GOD_TIER (DPR)** |
| **BLOODLUST** | Gain 1 Action on kill (1/Turn) + 5 Temp HP. | Martial Multi-Attacker / Sorlock. | **GOD_TIER (Action)**|
| **HILL_GIANT** | Sets **STR to 21**. | Early-game Tavern Brawler (Act 1). | **S_TIER (DPR)** |
| **BATTLEMAGE** | Gain 3 Arcane Acuity (+3 to Spell DCs). | Control Casters (Hold Person/Monster).| **S_TIER (Control)** |
| **VIGILANCE** | +5 Initiative; Cannot be surprised. | Low-DEX / High-Impact builds. | **S_TIER (Init)** |
| **COLOSSUS** | Gain Enlarge (1d4 extra dmg); Stat/Check Adv. | High-DPR martials / Throw builds. | **A_TIER (DPR)** |
| **VICIOUSNESS** | Reduces Crit Threshold by 1. | Rogue Assassin / Crit-Fighter. | **A_TIER (Crit)** |
| **PEERLESS_FOC**| Adv on Conc. Saves; Immune to Paralyze. | Haste/Hold Casters. | **A_TIER (Sustain)** |
| **RESISTANCE_O**| Resistance to ALL damage types. | High-tier survival / solo runs. | **A_TIER (Tank)** |
| **GUILE_MAST** | Lvl 1/2 Spell Slots become Proficiency bonus.| Support Casters (Bard/Cleric). | **B_TIER (Slot)** |
| **BARKSKIN** | Sets AC to 16. | Low-AC Druids / Monks / Wizards. | **B_TIER (AC)** |
| **HEROISM** | +10 Max HP; Gain Blessed effect. | Early-game frontline sustain. | **B_TIER (Tank)** |
| **SEE_INVIS** | See invisible entities within 9m. | Anti-stealth / Boss detection. | **B_TIER (Util)** |

---

## ⚡ Matrix B: Strategic Sourcing Logic

| Elixir_ID | Acquisition Point | Optimization Value |
| :--- | :--- | :--- |
| **HILL_GIANT** | Ethel (Act 1) - Stock 3 per long rest. | Mandatory for Act 1 Monks/Barbarians. |
| **CLOUD_GIANT** | Derryth/Roah (Act 3) - Global scaling. | The "Act 3 Floor" for STR Builds. |
| **BLOODLUST** | Roah Moonglow (Act 1/2). | Best used when fighting multiple mobs. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "CONSUMABLES_V13.2",
  "manifest_ref": "vanguard_manifest.json#CONSUMABLES",
  "patch_baseline": "8_HOTFIX36",
  "elixir_logic": {
    "STR_HILL": {"fixed_value": 21, "stat": "STR"},
    "STR_CLOUD": {"fixed_value": 27, "stat": "STR"},
    "BLOODLUST_HM": {"extra_action_on_kill": 1, "extra_multi_attack_hm": false},
    "BATTLE_MAGE": {"arcane_acuity_stacks": 3}
  },
  "optimization_priorities": {
    "STR_DPR": "STR_CLOUD",
    "SPEED_CLEAR": "BLOODLUST",
    "BOSS_SHUTDOWN": "BATTLEMAGE_POWER"
  }
}
```
