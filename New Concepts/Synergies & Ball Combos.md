---
title: Synergies & Ball Combos
tags:
  - Synergies
  - Combos
  - Balls
  - Pins
  - NewConcepts
status: concept
related:
  - "[[New Ideas Hub]]"
  - "[[Bouncy Bally]]"
  - "[[Skill tree]]"
  - "[[Ball upgrades]]"
  - "[[Pin upgrades]]"
---
#Synergies #Combos #Balls #Pins #NewConcepts

Emergent interactions between [[Ball upgrades|Ball Types]], [[Pin upgrades|Pin Modifiers]], and [[Board upgrades|Board Tools]] designed to reward intentional loadout crafting over generic stat stacking. Every combo below builds on existing mechanics without duplicating [[Effects upgrades]] (`Overclock`, `Dupliball`, `Bouncy rage`).

---

# 1. Cross-Ball Reactions (Mid-Air & Pin-Mediated)

Instead of balls acting in isolated lanes, specific pairs trigger **emergent reactions** when they collide mid-air or touch the same pin within a short window (`0.4s`).

| Ball Pair | Reaction Name | Trigger Condition | Emergent Effect |
| :--- | :--- | :--- | :--- |
| `Ghost` + `Steel` | **Phantom Cannonball** | Fast `Ghost` passes through heavy `Steel` mid-air | `Steel` becomes phased for `1.5s`, inheriting `Ghost`'s `2×` speed while keeping `Steel`'s `3×` reward and `1.3×` size to smash extra pins. |
| `Beach` + `Sticky` | **Tar Bubble** | `Beach` grazes an active `Sticky` ball | Coats `Beach`'s wide `1.2×` radius in adhesive, scooping up `1–2` nearby `Basic` or `Marble` balls into a cluster that pops at the bottom slot for a `1.5×` cluster bonus. |
| `Basket` + `Chemical` | **Catalyst Dunk** | `Chemical` transfers its `+0.5` bonus onto an airborne `Basket` | `Basket`'s next `1.8×` high-arc bounce triggers a **shockwave** on landing, splashing `50%` of its accumulated bonus to all pins within a `1`-row radius. |
| `Trick` + `Marble` | **Slipstream Draft** | `Marble` passes within `1` pin-width of `Trick`'s deterministic path | Locks `Marble`'s random speed roll to its maximum value, reliably securing `Marble`'s **1st-arrival `2×` reward** when sequenced right after `Trick`. |
| `Gambler` + `Golden` | **Jackpot Rigging** | A `Golden` ball is active when `Gambler` finishes its drop | `Golden`'s aura rigs the 10-sector Roulette Wheel for that spin, converting all `×0` bust sectors into `×2` safety sectors. |

> [!example] Intentional Batch Sequencing
> Using **Batch Splitter** (`A`/`B` sub-slots), place `Trick` in `Batch A` and `Marble` in `Batch B` with a `0.2s` offset. `Trick` carves a predictable deterministic lane, and `Marble` drafts behind it to win the 1st-arrival `2×` race almost every cycle.

---

# 2. Pin-Ball Alchemy (Modifier × Ball Reactions) Don't overcomplicate it, this synergies should only affect the ball not the board pins

Specific [[Pin upgrades|Pin Modifiers]] react uniquely with matching ball physics, turning standard pins into combo engines:

### Faraday Arc (`Tesla` Pin + `Steel` Ball)
- **Trigger**: Heavy `Steel` hits a `Tesla` (`Z`) pin.
- **Effect**: Instead of only adding `+0.6 × batchHits`, `Steel` magnetizes the pin and fires a **lightning arc** to the nearest un-hit pin in the row below, pre-triggering that pin's modifier as if a ball struck it.

### Refraction Split (`Prism` Pin + `Ghost` Ball)
- **Trigger**: Tiny, high-speed `Ghost` procs a `Prism` (`2x`) pin's `25%` `2.5×` roll.
- **Effect**: `Ghost` refracts into a `0.1s` afterimage that strikes the **opposite side** of the same pin—doubling the pin's contact count without cloning the ball mid-flight.

### Gilded Blueprint (`Midas` Pin + `Constructor` Ball)
- **Trigger**: A `randomOnly` `Constructor` ball touches a `Midas` (`$`) pin.
- **Effect**: Upgrades the ball's `+1` [[Plans]] drop into a **Golden Plan** (counts as `2×` wall upgrade progress and permanently adds `+1` level to that `Midas` pin for the current run).

### Resonance Loop (`Echo` Pin + `Sticky` Ball)
- **Trigger**: `Sticky` lands `3` consecutive contacts on a single `Echo` (`x2`) pin.
- **Effect**: The third contact **overloads** the pin for the rest of the batch, radiating a temporary `+1` flat bonus aura to its two horizontal neighbors.

### Calculated Ricochet (`Zigzag` Pin + `Trick` Ball)
- **Trigger**: `Trick` hits a `Zigzag` (`<>`) pin configured with the **Pin Tweaker** (`30%` or `70%` directional bias).
- **Effect**: Guarantees an alternating left-right-left bounce if adjacent pins have opposing biases, letting players engineer a `4+` direction-change staircase down the center of the board.

> [!tip] Pin Tweaker Synergy
> The **Pin Tweaker** (`30%–70%` bias) is not just for steering toward `Double slots`—pairing opposing `30%` and `70%` biases on adjacent `Zigzag` and `Chain` pins creates a "pinball bumper" pocket that farms direction changes and consecutive modifier hits.

---

# 3. Build-Defining Archetypes Declined

Combining **Batch Slots (`1–4`)**, **Batch Splitter**, **Pin Modifiers**, and **[[Plans]] Walls** enables four distinct playstyles:

1. **The Pinball Piñata (High-Volume Chaos)**
   - **Core**: `Sticky` + `Chemical` + `Beach` | `Echo`, `Chain`, `Tesla` pins.
   - **Loop**: Slows drop velocity to keep 10+ balls airborne at once, spiking `batchHits` for `Tesla` and triggering multi-ball `Tar Bubble` clusters.
2. **The Speedrun Slingshot (1st-Arrival Burst)**
   - **Core**: `Ghost` + `Marble` + `Trick` | `Turbo`, `Zigzag` pins + `Rapid Recharge`.
   - **Loop**: Minimizes cooldowns (`0.35s` cap) and maximizes ball speed so `Marble` constantly cashes `2×` 1st-arrival payouts and `Streak` (`3`) resets rapidly.
3. **The High-Roller Casino (Controlled Variance)**
   - **Core**: `Gambler` + `Golden` + `Fortune Core` (Luck) | `Lucky`, `Prism`, `Midas` pins.
   - **Loop**: Scales Luck to boost `randomOnly` spawn odds and Roulette payouts, using `Golden` balls to rig `Gambler` wheels and `Prism` pins to multiply `Midas` hits.
4. **The Architect's Loom (Board-Sculpting Funnel)**
   - **Core**: `Constructor` + `Trick` + `Basket` | `Amplifier`, `Midas`, `Prism` + `Pin Tweaker` + `Plans` Walls.
   - **Loop**: Uses `Constructor` to farm `Plans` early, builds angled walls to seal off low-value outer lanes, and funnels every ball through a hyper-leveled **Kill Corridor** above a `Double slot`.

---

# 4. Combo Codex (Discovery Progression) Explore the idea with what's not declined

To encourage experimentation across runs rather than sticking to one optimal setup:
- **First-Time Discovery**: Triggering any Cross-Ball or Pin-Ball reaction for the first time pops a non-intrusive toast (`COMBO DISCOVERED: Phantom Cannonball!`) and unlocks its entry in the **Combo Codex**.
- **Codex Mastery**: Every `3` unique combos discovered grants `+1` permanent **Core** (or a small **Prestige Shard** bonus on [[Prestige|Ascension]]), giving players a reason to test weird combinations like `Beach` + `Ghost` or `Constructor` + `Midas`.

---

# Related Pages
- [[New Ideas Hub]]
- [[Game Modes & Challenges]]
- [[Active Gameplay & Mechanics]]
- [[Board Dynamics & Hazards]]
- [[Ball upgrades]]
- [[Pin upgrades]]
- [[Skill tree]]
