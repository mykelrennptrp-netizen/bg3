---
id: BIOLOGY_ORIGIN_REGISTRY
name: Origin & Companion Forensic Registry
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Origins
logic_type: UNIQUE_ATTRIBUTE_MAPPING
---

# 🕵️ Origin Registry: v13.2 High-Fidelity Standard (Patch 8)

This node governs the unique mechanical overrides granted by Origin selection. It has been forensically satiated to allow Gemini Pro to calculate the hidden "Origin Advantage" (e.g., Astarion's +1 Happy bonus or Karlach's Engine Heat).

> [!IMPORTANT]
> ### [WIKI_LOCK] Origin Logic
> - **Mechanical Exclusivity**: Origin traits (e.g., *Happy*, *Netherese Orb*) cannot be obtained by custom characters.
> - **Compatibility**: All Origin characters are locked to their specific Race and Background, but their Class remains 100% flexible (Respec possible).
> - **The Dark Urge**: The only Origin with a "Customizable" Race and Class while maintaining a unique mechanical layer (*Deathstalker Mantle*).

---

## 📊 Matrix B: Origin & Companion Registry

| Origin_ID | Race | Background | Primary Mechanical Truth | Optimization_Cap |
| :--- | :--- | :--- | :--- | :--- |
| **ASTARION** | High Elf | Charlatan | **HAPPY**: +1 to all Rolls/Saves (Post-Bite). | **S_TIER (Burst/Reliability)** |
| **DARK_URGE** | ANY | Haunted One | **DEATHSTALKER**: Invisibility on Kill (Mantle). | **GOD_TIER (Solo/Assas)** |
| **KARLACH** | Zariel Tiefl.| Outlander | **ENGINE_HEAT**: 1d4 Fire (Soul Coin scaling).| **S_TIER (Melee DPR)** |
| **GALE** | Human | Sage | **NETHER_ORB**: Permanent AoE Burst/Sustain. | **S_TIER (Wizard/Caster)** |
| **MINTHARA**| Lolth-Drow | Noble | **SOUL_BRANDING**: BA add 2d4 Fire damage. | **S_TIER (BA Utility)** |
| **LAE_ZEL** | Githyanki | Soldier | **MARTIAL_PROD**: Prof in Medium/Heavy Sword.| **A_TIER (Martial)** |
| **SHADOWHT**| High H-Elf | Acolyte | **WOLF_FEAR**: Disadv near wolves (Debuff). | **A_TIER (Support)** |
| **WYLL** | Human | Folk Hero | **RAPIER_MAST**: Unique Rapier synergy. | **B_TIER (Warlock)** |
| **HALSIN** | Wood Elf | Outlander | **CAVE_BEAR**: Unique high-HP Wildshape. | **B_TIER (Druid)** |
| **JAHEIRA** | High H-Elf | Soldier | **HIGH_INIT**: 1d4 Bonus to Initiative. | **A_TIER (Hybrid)** |
| **MINSC** | Human | Folk Hero | **BOO_BOND**: Unique Summon logic (Boo). | **B_TIER (Ranger)** |

---

## 📉 Matrix G: Granular Origin Progression (v13.2)

| Origin_ID | Lvl | Gain_ID | Type | Forensic Effect |
| :--- | :--- | :--- | :--- | :--- |
| **ASTARION** | 1 | **VAMP_BITE** | BONUS | d4 Piercing + 12 HP heal + **HAPPY** Buff. |
| **DARK_URGE**| 1 | **DEATH_INVIS**| PASSIVE | Invisibility (2 turns) on kill once per turn.|
| **GALE** | 1 | **ORB_BURST** | ACTION | Massive AoE Burst (Game Over trigger). |
| **KARLACH** | 1 | **SOUL_ENG** | PASSIVE | Add Fire dmg while Raging or HP < 25%. |
| **MINTHARA** | 1 | **SOUL_BRAND** | BONUS | Target ally deals extra 2d4 fire on hit. |
| **JAHEIRA** | 1 | **HARPER_INIT**| PASSIVE | Permanent +1d4 to Initiative rolls. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "BIOLOGY_ORIGIN_V13.2",
  "manifest_ref": "vanguard_manifest.json#BIOLOGY",
  "patch_baseline": "8_HOTFIX36",
  "origin_overrides": {
    "ASTARION": {"happy_bonus": 1, "ascended": {"dmg": "1d10_Necrotic"}},
    "KARLACH": {"soul_coin_dmg": "1d4_Fire", "berserker_synergy": true},
    "DARK_URGE": {"mantle_invis_per_turn": 1, "slayer_form": true},
    "GALE": {"netherese_orb_unlock": "ACT_2_FINALE"},
    "MINTHARA": {"soul_branding_cost": "BONUS_ACTION"},
    "JAHEIRA": {"initiative_bonus": "1d4"}
  }
}
```
