#Balls #SkillTree

Ball upgrades unlock specialized [[Ball types]], increase per-ball [[Ball quantity|Quantity]], [[Ball value|Value]], and [[Ball speed|Speed]], and combine with **Individual Ball Cooldowns** and **Luck** mechanics.

# Ball Management & Cooldowns
- **Batch Configuration Grid**: Unlocked non-random balls appear in a compact `3×3` selector grid (`9` configurable balls) and can be assigned to any unlocked batch slot (`1`–`4`) or split sub-slot (`A` / `B`). Changing a slot's ball disables `Auto` until re-enabled.
- **Individual Ball Cooldowns**: Every ball type has a predefined base cooldown configured in its `BallDefinition` asset (editable in `Tools/Bouncy Bally/Editor`), displayed as read-only values inside Batch Configuration.
- **Effective Cooldown Formula**:
  $$\text{Cooldown} = \max\Big(0.35\text{s},\ \text{BaseCD} \times (1 - \min(0.85,\ \text{GlobalCD} + \text{BallCD} + \text{PrestigeCD}))\Big)$$
  - Cooldown reduction comes from **Ball Cooldown** (`-10%`/lv, max 3 levels, requires `Basic Ball Value`), **Rapid Recharge** (`-15%`/lv, max 3 levels, requires `Batch 2`), and **Chrono Drive** (`-10%`/lv, max 5 levels) in [[Prestige]].
- **Caps**: Ball count caps at `250` per ball type (`1` min) and Ball speed caps at `10` (`0.1` min, boosted up to `16` in flight by **Turbo** pins).

# Implemented Ball Types
- **Starter**:
  - **Basic Ball**: `startsUnlocked = 1`, value `1`, count `3`, speed `0.6`, base CD `2.2s`.
- **Configurable Unlockable Balls** (`3×3` grid):
  - **Basket Ball** (`3.0s` CD): High arc (`1.8×` bounce), `0.7×` speed, `+0.25` flat pin bonus per contact.
  - **Beach Ball** (`3.6s` CD): Large (`1.2×` size), `0.5×` speed, `2×` reward multiplier.
  - **Ghost Ball** (`1.4s` CD): Fast & small (`2×` speed, `0.6×` size), `0.5×` reward multiplier.
  - **Steel Ball** (`4.2s` CD): Heavy (`1.3×` size, `0.2×` speed, `0.3×` bounce), `3×` reward multiplier.
  - **Trick Ball** (`2.0s` CD): Deterministic first bounce direction (`firstBounceRight`).
  - **Sticky Ball** (`3.2s` CD): `0.8×` speed, `30%` base chance (Luck-scaled) to bounce up to `3` contacts on a pin.
  - **Chemical Ball** (`2.6s` CD): Every `3` pin contacts, transfers `+0.5` pin bonus to another active ball (or itself) with a chemical reaction arc.
  - **Marble Ball** (`2.4s` CD): `0.8×` base speed with `+0–0.6` random speed variation; the first ball to arrive in a batch earns `2×` reward.
- **Surprise / Random-Only Balls** (`randomOnly = 1`, replace any spawned ball via Luck-scaled probability):
  - **Golden Ball** (`1%` base chance): `10×` reward multiplier.
  - **Constructor Ball** (`2%` base chance): Wears a yellow hard hat and awards `+1` [[Plans]] per landing.
  - **Gambler Ball** (`2%` base chance): Opens the **Roulette Panel** (`30% ×0`, `40% ×1`, `20% ×5`, `10% ×10`) upon landing; high-multiplier sector weights (`×5`, `×10`) scale with **Luck**.

# Related Pages
- [[Ball quantity]]
- [[Ball speed]]
- [[Ball types]]
- [[Ball value]]
