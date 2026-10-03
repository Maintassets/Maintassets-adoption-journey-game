# MAINTASSETS — Adoption Journey Game

## 1. Overview
**MAINTASSETS — Adoption Journey** is a single-file, browser-based interactive exhibition game. The player moves four transformation dimensions from **Origin** to **Digital State / Destination** while managing **Value, Risk and Performance**.

The game is a business-transformation metaphor rather than a literal transport puzzle. Its central message is:

> Leadership defines the goal. Assets define the need. Data creates the insight. Technology enables execution. The real measure of transformation is the business outcome.

Everything is contained in one HTML file: HTML, CSS, JavaScript, embedded artwork/images/logo, animation, audio generation and local-storage progress.

---

## 2. Four Dimensions

| Dimension | Role | Meaning |
|---|---|---|
| **Leadership Engagement** | Organisation goal | Sets direction and ensures every decision serves the business goal |
| **Assets** | Foundation | Operational/physical assets that need to create value |
| **Data** | Insight | Information that explains asset condition, performance and needs |
| **Technology** | Enabler | Technology selected to support the data and asset objectives |

The intended transformation sequence is:

**Leadership → Asset objective → Data → Technology → Execution → Business outcome**

---

## 3. Main Objective

The player must:

1. Move all four dimensions to the Digital State.
2. Respect the dependency rules.
3. Stay within the decision budget.
4. In Level 3, finish within 60 seconds.
5. Meet the level's Value, Risk and Performance targets.

Reaching the destination alone is **not** sufficient. If all four dimensions arrive but the business targets are missed, the level fails.

This supports the game's core message:

> **Going live digitally is not automatically the same as becoming digitalised.**

---

## 4. Vehicle Rules

The transfer vehicle carries a maximum of **2 dimensions**.

Valid payloads are:

- Leadership Engagement alone
- Leadership Engagement + one other dimension

Every attempted crossing consumes one decision, including invalid attempts.

### Mandatory rule

**Leadership Engagement rides every crossing.**

If a crossing is attempted without Leadership Engagement, it is rejected and produces a negative business impact.

---

# 5. Dependency Rules

## Level 1 — Foundation

Active dependency:

**Assets + Data**

Assets and Data cannot be left together without Leadership Engagement.

Message:

> Asset data must serve the organisation goal.

## Level 2 — Integration

Active dependencies:

**Assets + Data**  
**Data + Technology**

Data becomes the connecting element between asset requirements and technology.

Message:

> Decide the data first. Then choose the technology for it.

## Level 3 — Transformation

Same two dependencies:

**Assets + Data**  
**Data + Technology**

But Level 3 adds time pressure and stricter outcome targets.

Also displayed as a safe execution relationship:

**Assets + Technology = execution pair**

---

# 6. Levels

| Feature | Level 1 | Level 2 | Level 3 |
|---|---:|---:|---:|
| Name | Foundation | Integration | Transformation |
| Dependencies | 1 | 2 | 2 |
| Decisions | 7 | 8 | 8 |
| Hints | 3 | 2 | 1 |
| Clock | None | None | 60 sec |
| Value target | ≥60 | ≥65 | ≥72 |
| Risk target | ≤55 | ≤55 | ≤50 |
| Performance target | ≥58 | ≥65 | ≥72 |

### Level 1 — FOUNDATION
**Purpose:** Learn the basic Asset/Data relationship.

The briefing states:

> **1 rule to watch: Assets + Data.**

The player learns Leadership, dependency validation and metric consequences.

### Level 2 — INTEGRATION
**Purpose:** Connect Data and Technology.

The briefing states:

> **New rule: Data + Technology. Data will need a return trip.**

The player must now manage two connected dependencies.

### Level 3 — TRANSFORMATION
**Purpose:** Execute the integrated journey under pressure.

The briefing states:

> **Same rules — under pressure: 60-second clock, higher targets.**

The player has only one hint, eight decisions and a 60-second transformation window.

---

# 7. Starting Metrics

Every level starts at:

```text
Value        = 50
Risk         = 50
Performance  = 50
```

All metrics are clamped between **0 and 100**.

---

# 8. Valid Decision Impact

The non-Leadership dimension determines the positive impact.

| Selected dimension | Value | Risk | Performance |
|---|---:|---:|---:|
| Data | +5 | -5 | +4 |
| Assets | +4 | -4 | +5 |
| Technology | +3 | -3 | +6 |
| Leadership Engagement alone | +1 | -1 | +1 |

Format is:

**Value / Risk / Performance**

Examples:

### Data
`+5 / -5 / +4`

### Assets
`+4 / -4 / +5`

### Technology
`+3 / -3 / +6`

### Leadership alone
`+1 / -1 / +1`

---

# 9. Invalid Decision Impact

Invalid crossings produce:

```text
Value        -4
Risk         +9
Performance  -5
```

An invalid move also consumes a decision.

Therefore, experimenting with invalid routes has a real gameplay cost:

- Value falls
- Risk rises
- Performance falls
- Decision budget decreases
- The player can ultimately fail the business objective

The game treats invalid moves as **rework, false starts and poor alignment**.

---

# 10. Completion Logic

A level succeeds only when:

```text
All 4 dimensions are at Destination
        AND
Value >= level target
        AND
Risk <= level target
        AND
Performance >= level target
```

Examples:

### Level 1
```text
Value >= 60
Risk <= 55
Performance >= 58
```

### Level 2
```text
Value >= 65
Risk <= 55
Performance >= 65
```

### Level 3
```text
Value >= 72
Risk <= 50
Performance >= 72
```

---

# 11. Failure Conditions

## Missing Leadership
Popup:

**NO LEADERSHIP, NO GOAL**

Message:

> Without a goal, nothing moves. Only leadership decides where we go.

Lesson:

**EVERY DRIVE IS DECIDED BY LEADERSHIP**

## Assets + Data violation
Popup:

**DATA WITHOUT A GOAL**

Message:

> Asset data must serve the organisation goal. Without it, the whole effort fails.

Lesson:

**ALIGN ASSET DATA TO THE ORGANISATION GOAL**

## Data + Technology violation
Popup:

**TECHNOLOGY BEFORE DATA**

Message:

> Decide the data first. Then choose the technology for it.

## Destination reached but targets missed
The game explains that the system is live but the business outcome has not changed sufficiently.

The current failure explanation communicates:

> The system is live, but the wrong moves raised risk and eroded value — the business hasn't changed.

## Decision budget exhausted
The level fails when all allowed decisions are consumed before successful completion.

## Time up
Only Level 3 has a timer. At 60 seconds, the transformation window closes and the level fails.

---

# 12. Hints

| Level | Hints |
|---|---:|
| Level 1 | 3 |
| Level 2 | 2 |
| Level 3 | 1 |

Hints do not change the metrics.

### Level 1 hint
> Move Assets or Data first — never leave the two of them alone together.

### Level 2/3 hint
> Data conflicts with both Assets and Technology. Move Data first, and bring it back when you need to.

---

# 13. Transformation Meaning of Actions

The game translates crossings into business decisions.

### Forward

**Leadership**
> Leadership checks the direction.

**Assets**
> Asset goals set by leadership.

**Data**
> Data aligned to the organisation goal.

**Technology**
> Right technology chosen.

### Return

**Leadership**
> Leadership back to the floor.

**Assets**
> Asset needs re-validated.

**Data**
> Data re-aligned to the goal.

**Technology**
> Technology choice revisited.

The purpose is to make every move communicate a real transformation decision rather than just a puzzle action.

---

# 14. Success / Journey Completion

After a successful level, the game:

- stops gameplay,
- records the best decision count,
- unlocks the next level,
- displays the completion message,
- shows final metrics,
- plays the success sound.

### Level 1
**FOUNDATION COMPLETE — UNDERSTAND BEFORE YOU OPTIMIZE**

> Strong asset management starts with understanding what you have and how it connects. You’ve established the foundation for making informed asset decisions.

### Level 2
**INTEGRATION COMPLETE — CONNECT THE SYSTEM**

> Assets create value when data, people, and decisions work together. You’ve connected the critical elements needed to manage assets as a system.

### Level 3
**TRANSFORMATION COMPLETE — TURN INSIGHT INTO ACTION**

> Effective asset management turns insight into action—and action into sustained value. You’ve demonstrated the ability to balance value, risk, and performance under pressure.

### Final journey
**ASSET MANAGEMENT JOURNEY COMPLETE — BETTER ASSET MANAGEMENT. BETTER OUTCOMES.**

The journey is:

**Foundation → Integration → Transformation**

---

# 15. Special Execution Event

When **Assets + Technology** are both at the destination, the game can display an execution message.

This reinforces:

> Technology creates value when it is connected to the asset requirement and the information required to manage it.

---

# 16. Interface

## Header / HUD
Shows:

- MAINTASSETS branding
- Client-Side Independent Consultant tagline
- Level
- Decisions
- Time
- Best score

## Metrics
Shows:

- Value
- Risk
- Performance
- Level targets
- Visual meters

## Rule Bar
Shows current rules:

- Leadership Engagement requirement
- Active dependencies
- Assets + Technology execution pair
- Level 3 clock

## Playfield
Contains:

- Origin
- Destination / Digital State
- Adoption Corridor
- Transfer vehicle
- Selected cargo
- Dimension tiles

## Bottom controls
- HINT
- RESET
- LEVELS
- PLAY AGAIN

---

# 17. Controls

| Input | Action |
|---|---|
| Click a dimension | Select/deselect |
| Click vehicle / CROSS | Attempt transfer |
| Space | Cross |
| R | Reset |
| H | Hint |
| 1 | Leadership Engagement |
| 2 | Assets |
| 3 | Data |
| 4 | Technology |

Maximum selection is two dimensions.

---

# 18. Progress and Best Score

The game uses browser `localStorage`.

Unlocked-level key:

```text
ma-adoption-unlocked
```

After completing a level, the next level becomes unlocked.

The best result is based on the **lowest number of decisions**. Fewer decisions represent less rework.

---

# 19. Game State

The runtime state includes:

```text
left
right
side
selected
moves
elapsed
playing
locked
hints
value
risk
performance
```

Additional state handles:

- timer
- execution event
- unlocked levels
- best scores

---

# 20. Important JavaScript Functions

### `select(item)`
Handles selection and deselection. Maximum two items.

### `cross()`
Main gameplay controller. It increments decisions, validates Leadership, simulates the move, checks dependencies, applies metric impact, animates the vehicle and checks completion.

### `valid(bank)`
Checks active dependency rules.

### `applyDecisionImpact(ok)`
Updates Value, Risk and Performance.

### `meetsObjective()`
Checks the current level's outcome thresholds.

### `check()`
Determines success or failure after a completed transfer.

### `finish()`
Handles successful level completion, score storage and level unlocking.

### `fail()`
Handles failure, stops the clock and displays the reason and final metrics.

### `hint()`
Displays the level-specific hint.

### `showBriefing()`
Displays the level rules, targets, decision limit, hint count and clock before the level begins.

---

# 21. Audio

The game uses the browser **Web Audio API**, so no separate sound files are required.

Generated sounds include:

- Selection
- Loading cargo
- Vehicle movement
- Warning
- Success
- Failure

---

# 22. Single HTML Architecture

The game is intentionally self-contained.

The HTML contains:

```text
HTML
CSS
JavaScript
Embedded logo
Embedded artwork/images
SVG graphics
Animations
Web Audio
localStorage
Game rules
Game state
```

No separate asset directory is required.

This is particularly suitable for an exhibition laptop or offline demonstration.

---

# 23. Visual / Brand Design

The game is a MAINTASSETS-branded exhibition experience.

The interface includes:

- MAINTASSETS logo
- MAINTASSETS wordmark
- Client-Side Independent Consultant tagline
- Deep navy game environment
- Blue/cyan highlights
- Gold/amber action accents
- Light text and metric states
- Green success states
- Red failure states

The playfield is intentionally more intense than a normal corporate landing page so that it reads as a **game playground** while retaining the MAINTASSETS visual identity.

---

# 24. Digital vs Digitalised

The game's central business lesson is:

## Digital
A system has been implemented and is operational.

## Digitalised
The organisation's processes, decisions and outcomes have actually changed.

The game therefore requires:

```text
Digital State
+
Business Outcome
```

A successful player must demonstrate more than implementation.

The intended message is:

> **You might go live on digital, but that does not automatically mean you are digitalised.**

---

# 25. Recommended Exhibition Flow

### Step 1 — Start
Explain that the player must move the organisation from Origin to Digital State while balancing Value, Risk and Performance.

### Step 2 — Level 1
Let the visitor discover the Assets/Data dependency.

### Step 3 — Level 2
Point out the new Data/Technology dependency.

Ask:

> Why should technology follow the data requirement?

### Step 4 — Level 3
Let the visitor experience the 60-second pressure.

### Step 5 — Discuss the result
Use the final metrics to discuss:

- Did Value improve?
- Did Risk remain controlled?
- Did Performance improve?
- Did the organisation merely go live?
- Or did it actually change?

---

# 26. Example Valid Strategy

A representative efficient Level 2/3 route is:

```text
1. Leadership Engagement + Data →
2. Leadership Engagement ←
3. Leadership Engagement + Technology →
4. Leadership Engagement + Data ←
5. Leadership Engagement + Assets →
6. Leadership Engagement ←
7. Leadership Engagement + Data →
```

The exact player experience can differ because invalid decisions are allowed and have consequences.

The important strategic principle is:

> **Data must be positioned carefully because it participates in both dependency relationships.**

---

# 27. Design Philosophy

The game combines three layers:

### Puzzle
Can the player solve the dependency problem?

### Business simulation
Do decisions improve Value, Risk and Performance?

### Transformation story
Does the player understand that Technology is an enabler rather than the starting point?

This makes the game suitable for a consulting/exhibition environment.

---

# 28. Quick Reference

```text
DIMENSIONS
Leadership Engagement
Assets
Data
Technology

VEHICLE CAPACITY
2

MANDATORY
Leadership Engagement

LEVEL 1
Foundation
Assets + Data
7 decisions
3 hints
V ≥ 60
R ≤ 55
P ≥ 58

LEVEL 2
Integration
Assets + Data
Data + Technology
8 decisions
2 hints
V ≥ 65
R ≤ 55
P ≥ 65

LEVEL 3
Transformation
Assets + Data
Data + Technology
8 decisions
1 hint
60 seconds
V ≥ 72
R ≤ 50
P ≥ 72

STARTING METRICS
Value = 50
Risk = 50
Performance = 50

INVALID MOVE
Value -4
Risk +9
Performance -5
```

---

# 29. Final Summary

The MAINTASSETS Adoption Journey is built around:

**Leadership → Assets → Data → Technology → Execution → Outcome**

The player progresses through:

**FOUNDATION → INTEGRATION → TRANSFORMATION**

The game rewards:

- correct sequencing,
- leadership alignment,
- useful data,
- appropriate technology,
- controlled risk,
- improved value,
- improved performance,
- and efficient decision-making.

Most importantly, it demonstrates that:

> **Technology implementation is only one part of transformation. Real digitalisation happens when leadership, assets, data and technology work together to produce better business outcomes.**
