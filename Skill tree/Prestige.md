#Prestige #Ascension

The Prestige (**Ascension**) system is accessed from the Settings menu (`PRESTIGE` button) and allows the player to reset their current run in exchange for **Prestige Shards**, **bonus Cores**, and permanent meta-progression upgrades.

# Ascension Threshold & Shard Formula
- **Requirement**: `RunEarned >= $2,500` in the current run.
- **Pending Prestige Shards**:
  $$\text{PendingShards} = \begin{cases} 0 & \text{if } \text{RunEarned} < 2500 \\ \max\left(1, \left\lfloor \left(\frac{\text{RunEarned}}{2500}\right)^{0.45} \right\rfloor\right) & \text{otherwise} \end{cases}$$
- **Next Shard Threshold**:
  $$\text{NextThreshold} = \left\lceil 2500 \times (\text{PendingShards} + 1)^{1 / 0.45} \right\rceil$$

# Ascension Bonuses
- **Global Payout Multiplier**: Every total Prestige Shard earned permanently grants `+25%` global payout (`PrestigeMultiplier = 1 + TotalPrestigeShardsEarned × 0.25`), even after spending shards on upgrades.
- **Bonus Cores**: Each ascension awards **`+2` bonus Cores** to spend on [[Lootboxes upgrades|Lootbox Capsules]].

# What Resets vs. What Persists

| Resets on Ascension | Persists Across Ascensions |
| :--- | :--- |
| Current Money & `RunEarned` | `PrestigeCount`, spendable & total `PrestigeShards` |
| Income/min & `LastBatch` | All 4 Permanent Prestige Upgrade levels |
| Active airborne balls & batch states | Current **Cores** (`+2` per ascension) & claimed Goal IDs |
| [[Skill tree]] levels & unlocked balls | [[Lootboxes upgrades]] rewards & owned Pin Modifiers (unequipped to inventory) |
| Batch slots (`1` unlocked, `0` split) | Constructor [[Plans]] (`PlayerPrefs`) |
| Board rows (reset to `6`) & slot multipliers | Workshop auto-unlock if **Master Tinkerer** Lv 1+ is owned |
| Pin levels, directional tuning, & `PinTweakerUnlocked` | — |
| Run Goal metrics (`Earned`, `BestBatch`, `Batches`, `DistinctModules`) | — |

# Permanent Prestige Upgrades

| Upgrade | Max Lv | Shard Cost Formula | Effect per Level | Max Total Effect |
| :--- | :---: | :--- | :--- | :--- |
| **Golden Momentum** | `10` | `1 + Lv` (`1, 2, …, 10`) | `+50%` Base Ball Value | `×6.0` Base Ball Value |
| **Chrono Drive** | `5` | `1 + Lv` (`1, 2, …, 5`) | `-10%` Batch Cooldown & `+15%` Ball Speed | `-50%` Cooldown (to `85%` global cap) & `+0.75` Speed |
| **Master Tinkerer** | `4` | `2 + 2 × Lv` (`2, 4, 6, 8`) | Start runs with Workshop unlocked & `+1` Module Slot | Workshop unlocked at start & `7` total Module Slots |
| **Fortune's Blessing** | `10` | `2 + 2 × Lv` (`2, 4, …, 20`) | `+12%` Luck & `+1` Base Slot Bonus | `+120%` Luck & `+10` Base Slot Bonus |
