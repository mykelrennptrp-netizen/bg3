---
id: RULES_PROFICIENCY
name: Proficiency Scaling Matrix
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Proficiency
logic_type: SCALING_MODIFIER
---

# 🎓 Proficiency: v13.2 High-Fidelity Standard (Patch 8)

This node governs the binary scaling bonus of all characters. It has been forensically satiated with the Octa-Matrix Standard, including the **Level 1-12 Scaling Table**.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Proficiency Rules
> - **Scaling (SSoT)**: Proficiency Bonus (PB) is based on **TOTAL Character Level**, not Class Level.
> - **Impact**: Added to Attack Rolls, Saving Throws (if proficient), and Skill Checks (if proficient).
> - **Expertise**: Doubles the PB bonus (2x PB). Found primarily in Rogue and Bard classes.

---

## 📊 Matrix A: Proficiency Bonus (PB) Scaling Table

| Total_Level | Proficiency_Bonus | Forensic_Impact |
| :--- | :--- | :--- |
| **1 - 4** | **+2** | Early-game baseline. |
| **5 - 8** | **+3** | Mid-game tactical spike. |
| **9 - 12** | **+4** | End-game nuclear scaling. |

---

## 📈 Matrix C: Expertise & Specialized Math

| Feature_ID | Formula | Impact |
| :--- | :--- | :--- |
| **PROFICIENCY** | `1 * PB` | Standard skill/attack bonus. |
| **EXPERTISE** | `2 * PB` | Highest possible non-magical skill bonus (+8 at Lv 9). |
| **REMARK_ATH** | `ceil(0.5 * PB)`| Champion Fighter bonus to physical checks. |
| **JACK_OF_ALL** | `floor(0.5 * PB)`| Bard bonus to non-proficient checks. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "PROFICIENCY_V13.2",
  "manifest_ref": "vanguard_manifest.json#ENGINE",
  "patch_baseline": "8_HOTFIX36",
  "scaling_table": {
    "1": 2, "2": 2, "3": 2, "4": 2,
    "5": 3, "6": 3, "7": 3, "8": 3,
    "9": 4, "10": 4, "11": 4, "12": 4
  },
  "mechanics": {
    "expertise_multiplier": 2,
    "jack_of_all_trades": 0.5,
    "remarkable_athlete": 0.5
  }
}
```
