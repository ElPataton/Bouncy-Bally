#Pins #SkillTree

Pins form the triangular Galton board and accumulate contact bonuses on every ball bounce. Pin tools unlock via the **Workshop** skill (`$225`, or automatically at run start with [[Prestige]] **Master Tinkerer**).

# Pin Leveling & Bulk Pin Upgrading
- **Level Scaling**: Each pin starts at Level `0` (`+0` bonus) and gains `+0.1` multiplier bonus (`+10%`) per level. Upgrade cost is `ceil(10 × 1.6^level)`.
- **Pin Workshop Bulk Upgrade Modes** (cycle via the Mode button next to `UPGRADE`):
  - **`UPGRADE x5`** (Default): Upgrades the selected pin up to 5 times (falling back to the 5 cheapest upgradable pins on the board).
  - **`x1 PIN`**: Upgrades the selected pin once (or the cheapest pin if none is selected).
  - **`ROW`**: Upgrades every pin in the selected pin's row (or the cheapest upgradable row) in one transaction.
  - **`MAX ALL`**: Upgrades the cheapest upgradable pins across the entire board until funds run out (safety cap: `200` purchases per click).
- **Hold-to-Upgrade**: Holding the `UPGRADE` button repeats the active upgrade mode (`0.28s` initial delay, then every `0.09s`).
- **Direct Board Shortcuts**:
  - `Click`: Select pin (or equip/remove an armed module).
  - `Double-Click`: Upgrade clicked pin by 1 level.
  - `Shift + Click`: Upgrade the entire row containing that pin.
  - `Ctrl + Click`: Trigger `Max All` across the board.

# Pin Tweaker (Directional Tuning)
- Unlocked by the **Pin Tweaker** skill (requires Workshop).
- Shifts left/right bounce probability in `5%` (`0.05`) steps within `30%`–`70%` bounds (`±4` steps max).
- Cost formula: `ceil(50,000 × 1.1^(purchases^2))` — every purchase increments the counter, including reversing direction.
- **Bias Synergy**: Equipped Pin Modifiers scale their effect `amount` by `1 + |RightChance - 0.5| × 2 × biasSynergy` (up to `+12%` at `30%` or `70%` for `0.3` biasSynergy).

# Pin Modifiers (10 Unique Modules)
Players start with `3` equipped module slots (`+1` per level of Prestige **Master Tinkerer**, up to `7`). Modules are unlocked once from [[Lootboxes upgrades|Lootbox Capsules]] and can be freely equipped/removed in the Pin Workshop.

| Modifier | Symbol | Effect Type | Parameters | Behavior |
| :--- | :---: | :--- | :--- | :--- |
| **Amplifier** | `+` | `AddBonus` | `amount: 1`, `biasSynergy: 0.3` | Adds `+1` bonus on every hit. |
| **Lucky** | `?` | `LuckyBonus` | `amount: 5`, `chance: 0.2`, `biasSynergy: 0.3` | `20%` chance (Luck-scaled) for `+5` bonus. |
| **Echo** | `x2` | `Echo` | `amount: 2`, `biasSynergy: 0.3` | Multiplies the current contact bonus by `2×`. |
| **Streak** | `3` | `Streak` | `amount: 4`, `hitThreshold: 3`, `biasSynergy: 0.3` | Every 3rd batch hit on this pin adds `+4`. |
| **Zigzag** | `<>` | `Alternating` | `amount: 0.5`, `biasSynergy: 0.3` | Adds `+0.5 × alternations` (direction changes). |
| **Chain** | `++` | `Chain` | `amount: 0.4`, `biasSynergy: 0.3` | Adds `+0.4 × chain` (consecutive modified pins hit). |
| **Midas** | `$` | `GoldenTouch` | `amount: 2.5`, `biasSynergy: 0.3` | Adds `+3.75` (`amount × 1.5`) golden bonus on every hit. |
| **Prism** | `2x` | `Splitter` | `amount: 1.5`, `chance: 0.25`, `biasSynergy: 0.3` | Adds `+1.5` bonus and `25%` chance (Luck-scaled) to `2.5×` the contact bonus. |
| **Turbo** | `>>` | `Accelerator` | `amount: 1.2`, `biasSynergy: 0.3` | Adds `+1.2` bonus and accelerates the ball by `+22%` (up to speed `16`). |
| **Tesla** | `Z` | `Capacitor` | `amount: 0.6`, `biasSynergy: 0.3` | Adds `+0.6 × batchHits` on this pin. |

# Related Pages
- [[Pin value %]]
- [[Pin types]]
