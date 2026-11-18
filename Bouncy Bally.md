#BouncyBally

An incremental physics-style Galton board (Plinko) game where batches of balls drop through a triangular grid of pins, accumulating contact bonuses and landing in bottom multiplier slots to earn money.

# Premise
Balls spawn at the top of the board and bounce row by row down to the bottom payout slots. Each pin contact adds to the ball's bonus multiplier (enhanced by Pin Levels, Pin Modifiers, and Directional Tuning), and landing in a slot multiplies the payout by the slot's multiplier and global/prestige factors. Earnings fund the [[Skill tree]], Pin Workshop upgrades, Lootbox Capsules, and [[Prestige|Prestige Ascension]].

# Core Systems
- **[[Skill tree]]**: Interactive webbed upgrade graph (`[[Upgrades.canvas]]`) covering [[Board upgrades]], [[Ball upgrades]], [[Pin upgrades]], and [[Lootboxes upgrades]].
- **Batch Slots & Batch Splitting**: Unlock up to 4 independent batch slots (`Batch 1`–`Batch 4`) and split them with **Batch Splitter** (Lv 1–4) so a single slot assigns and launches 2 ball types together with interleaved drops and summed cooldowns.
- **Individual Ball Cooldowns**: Every ball type has its own predefined base cooldown (`1.4s`–`4.2s`) configured on its ball asset (`Tools/Bouncy Bally/Editor -> Balls`), and benefits from Skill Tree cooldown upgrades (**Ball Cooldown**, **Rapid Recharge**) and Prestige (**Chrono Drive**) down to a `0.35s` minimum per ball.
- **Pin Workshop & Bulk Pin Upgrading**: Upgrade individual pins (`+0.1` multiplier bonus per level), equip unique Pin Modifiers (up to `3` base module slots, expandable to `7` via Prestige), tune left/right bounce probabilities (`30%`–`70%`), and bulk-upgrade pins using **Upgrade x5**, **Row**, **Max All**, and **Hold-to-Upgrade** (plus `Double-Click`, `Shift+Click`, and `Ctrl+Click` directly on pins).
- **[[Lootboxes upgrades|Lootbox Capsules]] & [[Achievements|Goals]]**: Complete one-time run Goals to earn **Cores**, then open **Starter**, **Tinker**, and **Charged** Capsules (using Cores or Money) with an animated 3-phase reveal overlay to unlock unique Pin Modifiers and permanent stat boosts.
- **Roulette Panel**: Landing a **Gambler Ball** opens an arcade 10-sector Roulette Wheel (`30% ×0`, `40% ×1`, `20% ×5`, `10% ×10`) whose high-tier odds scale with **Luck**.
- **[[Prestige|Prestige Ascension]]**: Once `RunEarned >= $2,500`, ascend for **Prestige Shards** (`floor((RunEarned / 2500)^0.45)`), a permanent `+25%` global multiplier per total shard earned, `+2` bonus Cores per ascension, and 4 permanent Prestige Upgrades.

# Payout Formula
Each landed ball pays out:
$$\text{Payout} = \text{BallValue} \times (1 + \text{AccumulatedPinBonus}) \times \max(1, \text{SlotMultiplier} + \text{SlotBonus}) \times \text{RewardFactor}$$

Where:
- `BallValue = max(0.1, (StartingValue + GlobalValue + BallValue) × PrestigeValueMultiplier)`
- `SlotMultiplier = BaseSlotMultiplier(column) × 2^(DoubleSlotsLevel)`
- `RewardFactor = GlobalReward × BallReward × PrestigeMultiplier × PayoutMultiplier × PulseFactor × BallBehaviorFactor`
