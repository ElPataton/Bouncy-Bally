---
title: Board Dynamics & Hazards
tags:
  - BouncyBally
  - NewConcepts
  - Board
  - Hazards
status: brainstorm
---
#BouncyBally #NewConcepts #Board #Hazards

Dynamic spatial zones, moving/reactive obstacles, and push-your-luck hazards that make the Galton board feel alive—giving players interesting routing decisions rather than a static triangle of pegs.

> [!important] Design Goal
> Every board element should create **spatial variety and risk-reward tension**, interacting naturally with [[Active Gameplay & Mechanics]] and [[Pin upgrades]].

---

# 1. Dynamic Board Zones

Board zones are spatial territories overlaid on sections of the Galton grid, encouraging players to aim drops or tune [[Pin upgrades|Directional Tweakers]] to exploit (or avoid) them.

### Wind Tunnel Lanes
- **Behavior**: A gentle vertical or diagonal air current spanning 2–3 columns on one flank of the board.
- **Physics**: Lighter balls drift strongly with the wind, while heavy balls (like *Steel*) resist it and punch straight through.
- **Tactical Use**: Steers balls toward outer high-multiplier slots—or pushes them away if the wind direction flips every `20s`!

### Ice Patch vs. Trampoline Quadrants
- **Ice Patch**: A frosted 3-pin triangle where balls slide off pins with `1.4x` speed and low bounce—ideal for rapid slot cycling and **Call-Your-Shot** speedruns.
- **Trampoline Zone**: A springy rubberized patch that bounces balls upward at `1.5x` restitution, trapping them for extra pin contacts before they escape.

### Shifting Fever Spotlight
- **Behavior**: A glowing spotlight drifts slowly across 3–4 pins at a time.
- **Effect**: Every pin contact inside the spotlight charges a **Fever Gauge**. Reaching `100%` triggers a `6s` **Spotlight Frenzy** where the spotlight expands to cover an entire row and doubles contact speed.

> [!tip] Zoning Synergy
> Combine a **Trampoline Zone** with [[Active Gameplay & Mechanics#Kinetic Table Nudge (Tilt Mechanic)|Kinetic Table Nudge]] to keep high-value balls bouncing inside the **Fever Spotlight**!

---

# 2. Moving & Reactive Obstacles

### Swinging Pendulum Gate
- **Placement**: Suspended across the middle rows (Row 3–4), swinging smoothly left and right on a predictable beat.
- **Interaction**:
  - **Deflection**: Striking the pendulum flings the ball sharply sideways toward the outer edges of the board.
  - **Clean Thread**: Passing cleanly through the gap while the pendulum is at the opposite side awards a **Thread the Needle** bonus (`+1.0` flat pin bonus).

### Pinball Pop-Bumpers
- **Placement**: Replaces 1–2 selected pins with spring-loaded **Pop-Bumpers** (on a short `1.5s` internal recharge).
- **Interaction**: Hitting a charged Pop-Bumper blasts the ball upward/diagonally with a crisp *ding!*, awards a flat bonus, and emits a tiny radial knockback that can knock neighboring balls into mid-air collisions.

### Portal Tubes (One-Way Warps)
- **Placement**: Linked Entry/Exit rings—for example, an Entry portal in Row 5 (bottom-center) that warps balls back up to Row 2 (top-left or top-right).
- **Payoff**: Lets balls run **extended multi-row loops** for massive `AccumulatedPinBonus` before finally dropping into the payout slots.
- **Limit**: A ball can only use a Portal Tube once per drop (`1` warp tag) to prevent infinite loops.

### Armored Pinata Pins
- **Behavior**: Special crystalline pins that take `3` hits to crack open.
- **Payoff**: On the 3rd hit, the pin shatters in a **Pinata Burst**, spawning `3` tiny **Spark Sub-Balls** (worth `0.4x` base value each) that scatter across the lower rows and land in multiple slots simultaneously. Regenerates after `10s`.

---

# 3. Risk-Reward Triggers & Hazards

### The Trapdoor Pot (Push-Your-Luck Center Slot)
- **Toggleable Mode**: Players can arm the **Trapdoor** on the center `×1` slot.
- **Mechanic**:
  - Any ball that falls into the armed Trapdoor pays `$0` and **empties the Pot**...
  - ...but every ball that *dodges* the Trapdoor into any other slot adds `+10%` of its payout into a growing **Danger Pot**!
  - The first ball to land in an outer `×5` or `×10` slot while the Pot is active claims the entire Danger Pot.

> [!example] Push-Your-Luck Tension
> Armed Trapdoor + **Micro-Flippers** or **Table Nudge** turns every center-drifting ball into a heart-pounding save—let the Danger Pot grow, or cash out on an edge slot!

### Thermal Overheat Pins
- **Mechanic**: Pins track rapid consecutive hits on a **Thermal Gauge** (`0` → `5`).
  - **Hits 1–3 (Warm)**: Pin glows amber and adds `+0.25` extra heat bonus per contact.
  - **Hit 4 (Red-Hot)**: Pin sizzles; the ball becomes **Ignited**, leaving a flame trail that scorches the next `2` pins for `1.5x` contact bonus.
  - **Hit 5 (Overheat)**: Pin vents steam and blasts the ball sideways at `2.0x` speed, resetting the pin's gauge to `0` (`3s` cool-down).

### Shifting Floor Dividers
- **Behavior**: Every `15s`, the dividers between the bottom payout slots smoothly slide half a column left or right, shifting where the high-multiplier jackpot pockets sit.
- **Gameplay Impact**: Prevents stale "set-and-forget" setups—players who actively adjust their **Dropper Aim** or **Call-Your-Shot** target ride the shifting jackpot wave for higher returns.

---

# Related Pages
- [[New Ideas Hub]]
- [[Active Gameplay & Mechanics]]
- [[Synergies & Ball Combos]]
- [[Game Modes & Challenges]]
- [[Bouncy Bally]]
- [[Board upgrades]]
- [[Pin upgrades]]
