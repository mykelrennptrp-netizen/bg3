---
id: LOGISTICS_INSPIRATION
name: Inspiration & Reroll Logistics
version: v13.2
patch_baseline: Patch 8 (Hotfix 36)
wiki_source: https://bg3.wiki/wiki/Inspiration
logic_type: RESOURCE_CONVERSION
---

# 🗯️ Inspiration: v13.2 High-Fidelity Standard (Patch 8)

This node governs the secondary reroll economy and XP overflow conversion. It has been forensically satiated with the Octa-Matrix Standard for Gemini Pro party-optimization.

> [!IMPORTANT]
> ### [WIKI_LOCK] Core Inspiration Rules
> - **Pool Limit (SSoT)**: The party shares a global pool of **4 Inspiration points**.
> - **Earning (SSoT)**: Earned by completing background-specific goals (e.g., Astarion/Charlatan, Gale/Sage).
> - **The Overflow (SSoT)**: When at 4 points, any further inspiration earned is automatically converted into **Experience (XP)**. 

---

## 📊 Matrix A: Logistics & Earning
| Feature | Mechanical Truth | Impact |
| :--- | :--- | :--- |
| **Max Capacity** | 4 Points | Stored at party level. |
| **Reroll Type** | Ability Check | Dialog/Exploration ONLY (No Combat). |
| **XP Conversion** | Automatic at Cap | Primary source of non-combat XP scaling. |
| **Background Map**| 12 Backgrounds | Each has unique triggers for earning. |

---

## 🔒 Layer 4: Hidden JSON Satiation Pod (Agent-Only)

```json
{
  "logic_id": "INSPIRATION_V13.2",
  "manifest_ref": "vanguard_manifest.json#LOGISTICS",
  "patch_baseline": "8_HOTFIX36",
  "mechanics": {
    "max_pool": 4,
    "shared_party_pool": true,
    "combat_utilization": false,
    "xp_conversion_enabled": true
  },
  "optimization_priorities": {
    "LEVEL_PUSH": "Earn Inspiration while at 4/4 to maximize XP gain.",
    "DIALOG_SECURITY": "Reserve 1 point for critical DC 20+ Dialog checks."
  }
}
```
