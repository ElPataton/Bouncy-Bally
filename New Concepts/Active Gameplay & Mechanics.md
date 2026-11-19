---
title: Active Gameplay & Mechanics
tags:
  - BouncyBally
  - NewConcepts
  - Gameplay
  - Physics
status: brainstorm
---
#BouncyBally #NewConcepts #Gameplay #Physics

Active, tactile mechanics designed to give players meaningful moment-to-moment agency during a run—turning *Bouncy Bally* from a purely passive Galton board into a skill-expressive physics playground while keeping automated play viable.

> [!important] Design Goal
> Every active mechanic should reward **timing, spatial awareness, and physics mastery** rather than just clicking a button for a flat `+10%` stat boost.

---

# 1. Skill-Shot Dropper (Aim, Spin & Power)

Instead of balls always spawning from a fixed center-top point, active players can control the **Dropper Hopper** directly.

### Lateral Aim & Drop Offset
- **Control**: Drag the hopper horizontally (or use `A`/`D`) across the top row before releasing a batch.
- **Payoff**: Lets players deliberately target specific upgraded pins, [[Board Dynamics & Hazards#Dynamic Board Zones|Dynamic Board Zones]], or outer high-multiplier slots.

### English / Spin Control
- **Control**: Flick left or right on release to impart **Spin** (`-100%` to `+100%`).
- **Physics**: Spin bends the ball's horizontal deflection angle on each pin contact, letting skilled players curve balls *around* center hazards or hug the outer edge.
- **Curve Bonus**: Crossing from the left third of the board to the right third (or vice versa) in a single drop awards a **Cross-Board Curve** multiplier (`+0.75` to `AccumulatedPinBonus`).

### Power-Drop Slingshot
- **Control**: Pull the hopper upward/backward and release to launch a **Charged Drop** at `1.6x` initial downward velocity.
- **Physics**: The first pin struck by a Power-Dropped ball emits a small **Kinetic Shockwave** that nudges nearby airborne balls and guarantees a crisp, high-energy bounce.

> [!tip] Auto-Launch Harmony
> When **AutoLaunch** is enabled, the hopper smoothly sweeps or uses the player's last aimed offset and spin preset—so manual skill shots set up your automated farm!

---

# 2. Tactile Board Controls (Pinball-Inspired Agency)

### Kinetic Table Nudge (Tilt Mechanic)
- **Control**: Press `Space` (or directional flick) to jolt the entire board slightly left, right, or upward.
- **Effect**: Applies a small impulse to every ball currently in flight—perfect for rescuing a high-value ball drifting toward a low-multiplier center slot or nudging two balls into a mid-air collision.
- **Risk-Reward (Tilt Meter)**: Each nudge adds `35%` to a **Tilt Meter** that decays over `4s`. Exceeding `100%` triggers a **Tilt Lockout** (`5s` where nudging is disabled and pin bonuses freeze for `2s`).

### Micro-Flippers (Second-Pass Paddles)
- **Control**: Unlockable pair of tiny flippers flanking the bottom-most row (`Z` / `/` or Left/Right Click).
- **Effect**: Snapping a flipper at the right moment bats a falling ball **back upward** into the lower-middle pins for a **Second Pass**.
- **Air-Time Bonus**: Each second pass adds `+1` to the ball's **Juggle Count**, granting `+0.5` bonus multiplier per juggle—capped at 3 juggles per ball to prevent infinite stalls.

### Magnetic Snag & Flick
- **Control**: Click and hold any airborne ball for up to `0.6s` to catch it in a brief stasis bubble, then flick the cursor to release it at a chosen angle.
- **Cooldown**: `6s` per charge (holds up to 2 charges).
- **Use Case**: Snag a high-payout ball and hurl it directly into a cluster of heavily upgraded pins or into another ball for a guaranteed **Billiard Clack**.

---

# 3. Mid-Air Physics & Skill Combos

### Mid-Air Billiard Collisions ("Clack!")
- **Trigger**: Whenever two airborne balls collide mid-flight (naturally, via Batch Splitter, or via Micro-Flippers).
- **Effect**: Both balls spark with a crisp audio-visual *Clack!*, exchange momentum, and gain `+1` **Ricochet Stack** (`+0.5` flat pin bonus per stack).
- **Cluster Chain**: 3+ collisions within `1.5s` trigger a **Chain Reaction** wave that temporarily widens pin hitboxes for `2s`.

### Call-Your-Shot (Slot Sniping)
- **Control**: Click any bottom payout slot to mark it as your **Called Target** (highlighted with a pulsing reticle).
- **Payoff**:
  - Landing a ball in the Called Target awards a **Bullseye Bonus** (`1.5x` slot payout) and shaves `0.25s` off that batch slot's active cooldown.
  - Calling outer low-probability slots (`×5`, `×10`) grants a higher Bullseye Bonus (`2.0x`) than center slots.

### Rhythm Dropper (Cadence Streak)
- **Mechanic**: A subtle rhythmic pulse rings around the dropper when a batch is ready.
- **Payoff**: Manually firing within the beat window builds a **Tempo Streak** (`1` → `5`). At `5` Tempo, the next batch launches as a **Synchronized Volley**—balls drop in a tight, shimmering formation that increases mid-air collision chances.

> [!example] Skill Combo Loop
> Aim a **Power-Drop** with right-spin → **Nudge** the board mid-flight to trigger a **Mid-Air Clack** → bat the surviving ball with a **Micro-Flipper** into your **Called Target** slot for a massive stacked payout and instant cooldown shave.

---

# 4. Active Hotbar Abilities

Active abilities sit on a 3-slot hotbar (`1`, `2`, `3`) with independent cooldowns—designed to create dramatic, high-chaos moments rather than passive background buffs.

| Ability | Cooldown | Duration | Active Effect |
| :--- | :---: | :---: | :--- |
| **Zero-G Burst** | `25s` | `2.5s` | Cuts gravity by `85%`, turning falling balls into floating pinball chaos that rack up rapid multi-pin contacts. |
| **Gravity Well** | `20s` | `3.0s` | Cursor-placed vortex anywhere on the board; pulls nearby balls into a tight orbit before flinging them outward at `1.8x` speed. |
| **Bullet Time** | `30s` | `4.0s` | Slows ball physics to `0.35x` speed while keeping **Aim**, **Flippers**, and **Magnetic Snag** at full speed for surgical combos. |

---

# Related Pages
- [[New Ideas Hub]]
- [[Board Dynamics & Hazards]]
- [[Synergies & Ball Combos]]
- [[Game Modes & Challenges]]
- [[Bouncy Bally]]
- [[Skill tree]]
