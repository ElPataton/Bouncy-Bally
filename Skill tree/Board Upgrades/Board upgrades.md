#Board #SkillTree

Board upgrades expand batch capacity, reduce cooldowns, boost Luck, unlock [[Pin upgrades|Pin Workshop]] tools, and scale board slot multipliers.

# Implemented Board Skills

| Skill | Effect | Max Lv | First Cost | Cost Growth | Prerequisite | Details |
| :--- | :--- | :---: | :---: | :---: | :--- | :--- |
| **Batch 2** | `UnlockBatch` (2) | `1` | `$1,000` | `1` | — | Unlocks Batch slot 2 |
| **Batch 3** | `UnlockBatch` (3) | `1` | `$7,500` | `1` | Batch 2 | Unlocks Batch slot 3 |
| **Batch 4** | `UnlockBatch` (4) | `1` | `$40,000` | `1` | Batch 3 | Unlocks Batch slot 4 |
| **Batch Splitter** | `SplitBatch` (`+1` split/lv) | `4` | `$450` | `3.5` | Batch 2 | Splits Batch 1–4 into sub-slots **A** & **B** |
| **Rapid Recharge** | `Cooldown` (`-15%`/lv) | `3` | `$180` | `2.4` | Batch 2 | Reduces all ball cooldowns (cap `85%` total) |
| **Ball Cooldown** | `Cooldown` (`-10%`/lv) | `3` | `$45` | `2.2` | Basic Ball Value | Early cooldown reduction across all balls |
| **Workshop** | `Workshop` | `1` | `$225` | `1` | — | Unlocks Pin Workshop & [[Lootboxes upgrades]] |
| **Fortune Core** | `Luck` (`+10%`/lv) | `3` | `$250` | `2.5` | Workshop | Boosts ball, pin, roulette, & capsule odds |
| **Pin Tweaker** | `PinTweaker` | `1` | `$5` | `1.61` | Workshop | Unlocks paid `±5%` pin direction tuning (`30%`–`70%`) |
| **Pin mult** / **Pin mult 2** | `PinBonus` (`+0.5`/lv) | `2` | `$12` | `2` | — | Global `+0.5` bonus added to every pin contact |
| **Double slots** | `SlotMultiplier` (`×2`) | `2` | `$12` | `2` | — | Doubles all bottom payout slot multipliers (`[[Mult]]`) |

# Key Mechanics
- **Batch Splitting**: Each level of **Batch Splitter** splits the next unlocked batch slot into two sub-slots (`A` and `B`). Split slots alternate spawns (`A, B, A, B...`), combine total ball counts, and sum the cooldowns of both assigned ball types (`GetCooldown(A) + GetCooldown(B)`).
- **Board Layout & [[Board size|Board Expansion]]**: The board starts with `6` rows (`7` slots: `{ 8, 4, 2, 1, 2, 4, 8 }`) and supports up to `8` rows (`9` slots). Pending row expansions apply automatically once no balls are airborne (`pendingBalls == 0`).
- **Luck Scaling (`Fortune Core`)**: Probabilities scale via `clamp01(baseChance × (1 + luck) + luck × 0.03)`. Global skill Luck caps at `2.5` (`3.0` total with [[Prestige]] **Fortune's Blessing**).
