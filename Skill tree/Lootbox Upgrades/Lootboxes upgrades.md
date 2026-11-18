#Lootboxes #Capsules #SkillTree

Lootbox Capsules provide a closed collection of `16` unique rewards—unlocking all `10` [[Pin upgrades|Pin Modifiers]] and `6` permanent run stat upgrades. Capsules unlock with the **Workshop** skill (`$225`) and are opened from the Pin Workshop (`CAPSULES` button).

# Core Mechanics
- **Dual Currency Payment**: Each capsule can be opened using **Cores** (earned from the `16` run Goals and `+2` per [[Prestige]] ascension) or **Money**. If the player has enough Cores, Cores are spent first; otherwise Money is used.
- **Draw Without Replacement**: All capsules share claimed reward IDs (`RewardCollection`). Once a reward is obtained, it is permanently removed from that run's pool and remaining drop percentages dynamically update.
- **Luck Scaling**: **Luck** (from **Fortune Core** and **Fortune's Blessing**) boosts the weight of rarer rewards in a capsule pool via `w × (1 + luck × (1 - w / maxWeight))`.
- **Opening Animation**: Opening a capsule triggers a 3-phase full-screen reveal overlay:
  1. **Charge & Shake** (`0.72s`): Card shakes and cycles `CHARGING CAPSULE...` → `DECODING REWARD...` → `UNLOCKING SEAL...`.
  2. **Burst Flash** (`0.22s`): White-to-gold flash and expanding glow.
  3. **Elastic Reveal** (`0.28s` bounce + particle burst): Displays reward title, emblem, and effect (`CLICK TO CONTINUE`, auto-closes after `1.8s` if unclicked).

# Capsule Tiers & Reward Pools

### 1. Starter Capsule (`1 Core` or `$250` — 5 Rewards)
- **Amplifier** Pin Module (`weight: 3`)
- **Lucky** Pin Module (`weight: 3`)
- **Turbo** Pin Module (`weight: 2.5`)
- **Polished Core**: `+1` Base Ball Value (`weight: 4`)
- **Spring Pegs**: `+0.4` Global Pin Bonus (`weight: 4`)

### 2. Tinker Capsule (`2 Cores` or `$1,200` — 6 Rewards)
- **Zigzag** Pin Module (`weight: 3`)
- **Streak** Pin Module (`weight: 2.5`)
- **Chain** Pin Module (`weight: 2.5`)
- **Tesla** Pin Module (`weight: 2`)
- **Amplified Chutes**: `+1.5` Global Slot Bonus (`weight: 3.5`)
- **Overdrive Coil**: `×1.25` Global Reward Multiplier (`weight: 2`)

### 3. Charged Capsule (`3 Cores` or `$5,000` — 5 Rewards)
- **Echo** Pin Module (`weight: 2.5`)
- **Prism** Pin Module (`weight: 2`)
- **Midas** Pin Module (`weight: 1.5`)
- **Hyper Core**: `+3` Base Ball Value (`weight: 3`)
- **Singularity Core**: `×1.5` Global Reward Multiplier (`weight: 1.5`)

# Related Pages
- [[Lootbox Store]]
- [[Lootbox Pins]]
- [[Lootbox powerups]]
- [[Auto lootbox]]
- [[Auto powerups]]
- [[Achievements]]
