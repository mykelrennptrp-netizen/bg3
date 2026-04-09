# Vanguard Forensic Rules: Honour Mode v13.2

This node governs the mechanical overrides and legendary triggers exclusive to **Honour Mode**, ensuring 100% forensic accuracy for the highest difficulty builds.

**Standard**: Octa-Matrix v13.2
**Patch Baseline**: Patch 8 (Hotfix 36)
**Agentic Logic**: Rule Override Enforcement

---

## ⚖️ Honour Mode: Rule Overrides

| Mechanic | Standard Logic | Honour Mode Logic | Forensic Rationale |
| :--- | :--- | :--- | :--- |
| **Haste Action** | Provides a full Action. | **RESTRICTED**: Provided action only allows 1 attack (No Extra Attack benefit). | Prevents extreme DPR scaling. |
| **Extra Attack** | Stacks across classes (e.g. Paladin/Warlock). | **NON-STACKING**: Paladin 5 / Bladelock 5 does NOT grant 3 attacks. | Correcting unintended synergy (Patch 8 lock).|
| **Bloodlust Action**| Provides a full Action. | **RESTRICTED**: Provided action only allows 1 attack. | Limits multi-kill runaway power. |
| **Legendary Actions**| None. | **ACTIVE**: Select bosses gain unique reactions/actions off-turn. | Forced tactical adaptation. |

---

## 👹 Legendary Action Matrix (Boss Counter-Logic)

| Boss | Legendary Action | Forensic Counter-Logic |
| :--- | :--- | :--- |
| **Owlbear** | Call of the Mate | Focus-fire mate or separate them via forced movement. |
| **Grym** | Adamantine Backlash | Utilize "Groggy" state; preserve reactions for movement. |
| **Inquisitor W'wargaz**| Mind-Claw of Tu'narath| Use summons to absorb "Mind-Claws"; break Concentration early. |
| **Ketheric Thorm**| Gaze of the Dead | Blindness/Fog Cloud to negate gaze proximity. |
| **Raphael** | Beguiling Dance | High WIS saves or "Calm Emotions" to prevent CC lock. |
| **Ansur** | Stormheart Chill | Cold resistance + Evasion for Breath logic. |
| **Orin the Red** | Murderous Strike | Break "Unstoppable" stacks via MM/Magic Missile or Multi-hit. |

---

## 🤖 Layer 4: Honour Mode JSON Pod (Agentic Ingestion)

```json
{
  "shard_id": "HONOUR_MODE_V13.2",
  "mechanic_overrides": {
    "HASTE_NERF": true,
    "EXTRA_ATTACK_STACKING_P5_W5": false,
    "BLOODLUST_NERF": true
  },
  "priority_optimization": {
    "ACTION_ECONOMY": ["FIGHTER_ACTION_SURGE", "SORCERER_METAMAGIC"],
    "UNSTOPPABLE_COUNTERS": ["MAGIC_MISSILE", "ARTISTRY_OF_WAR", "SCORCHING_RAY"]
  }
}
```
