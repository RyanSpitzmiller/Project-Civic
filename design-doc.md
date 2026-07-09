# Project [Civic Name/Number] — Race Car Design Document

**Author:** [Your Name]
**Started:** [Date]
**Status:** Pre-acquisition planning phase
**Platform (candidate):** [e.g., 1999-2000 Honda Civic Si, EM1 chassis]

> This document is a living record of every design decision made on this build, the reasoning behind it, and the data used to make it. It starts before the car exists and gets updated continuously. Treat every entry like you're explaining the decision to an engineering manager who will ask "why?"

---

## 1. Project Goals & Requirements

*Everything below traces back to this section. If a decision doesn't serve one of these goals, question it.*

**Primary use case:** [e.g., Autocross / Track days / Time attack / Wheel-to-wheel club racing]

**Target sanctioning body / class (if any):** [e.g., NASA Time Trial, SCCA Solo — this matters because it sets rules constraints]

**Performance targets:**
- Target curb weight: [e.g., under 2,400 lbs, down from ~2,650 lbs stock]
- Target power-to-weight: [fill in once engine plan is set]
- Target skidpad / lap time benchmark: [pick a reference car/time if known]

**Budget constraint:** [Total budget, or budget per phase]

**Non-negotiables:** [e.g., "must remain street-legal and drivable to track days" or "daily-drivability is not a constraint, full stripped race build"]

**Explicitly out of scope:** [e.g., "not chasing max horsepower, prioritizing chassis balance and driver feedback"]

---

## 2. Platform Research & Selection Rationale

*Why this car, not another. This section shows you can evaluate a platform analytically, not just because you like it.*

| Factor | Spec (stock) | Source |
|---|---|---|
| Curb weight | [XXXX lbs] | [factory manual / source] |
| Weight distribution (F/R) | [XX/XX %] | [source] |
| Wheelbase | [XX in] | |
| Track width (F/R) | [XX in / XX in] | |
| Suspension type (F) | [e.g., double wishbone] | |
| Suspension type (R) | [e.g., double wishbone] | |
| Engine | [code, displacement, layout] | |
| Stock power/torque | [XX hp / XX lb-ft] | |
| Drivetrain layout | [FWD/RWD/AWD] | |

**Why this platform (trade-off reasoning):**
> Example: "The EM1 Civic Si uses double-wishbone suspension front and rear, which is unusual for an economy car of its era and gives it superior camber control under load compared to strut-based competitors like the contemporary Civic DX. This makes it a stronger starting point for track use despite being FWD, which limits ultimate power potential compared to RWD platforms. Chose this over [alternative, e.g., Miata] because [reason — familiarity, parts cost, community support, etc.]."

**Known weaknesses to design around:**
> Example: "FWD layout means power delivery under cornering load will cause torque steer and understeer under power — front-end grip and diff behavior will be a priority design focus, not just power."

---

## 3. Subsystem Design Log

*This is the core of the document. One entry per major decision. Copy this block for every decision you make — big or small.*

### Entry format:
```
### [Subsystem] — [Decision Title]
Date: 
Goal this decision serves (from Section 1): 
Options considered: 
  - Option A: [description] — Pros / Cons
  - Option B: [description] — Pros / Cons
Decision: 
Reasoning: 
Supporting calculation/data (if any): 
Open questions / risks: 
```

### Worked example:

### Suspension — Spring Rate Selection (Front)
**Date:** [placeholder]
**Goal this decision serves:** Target skidpad performance; goal is track precision over ride comfort (Section 1)
**Options considered:**
- Option A: Stock spring rate (~2.5 kg/mm front) — Pros: cheap, comfortable; Cons: too soft for track, excess body roll
- Option B: Aftermarket coilovers, adjustable, ~6-8 kg/mm front — Pros: matches target use case, adjustable for tuning; Cons: cost (~$1,200-1,800), ride quality loss for street use
**Decision:** Option B — adjustable coilovers in the 6-8 kg/mm front range
**Reasoning:** Given the car will see dedicated track use (Section 1 goal), ride comfort is explicitly out of scope. Adjustability lets me tune understeer/oversteer balance over time rather than committing to one static rate before I have any seat time in the car.
**Supporting calculation:** [This is where you'd do a rough motion-ratio-adjusted wheel rate calc once you have real suspension geometry numbers — flag as TODO until you own the car]
**Open questions/risks:** Don't yet know actual corner weights — will revisit rate choice after scaling the car.

---

## 4. Calculations & Reference Data

*Track your math here, even rough hand-calcs. This is what shows engineering rigor, not just parts-swapping.*

- Weight distribution (measured, once available): TBD
- Corner weights: TBD
- Roll center height (front/rear): TBD — calculate from suspension pickup points once measured
- Anti-squat / anti-dive %: TBD
- Estimated lateral g target: TBD

*Recommended reference: Milliken & Milliken, "Race Car Vehicle Dynamics" — use this for the actual formulas once you get here.*

---

## 5. Before/After Data Log

*Fill in once the car is in hand. This is your proof-of-work section.*

| Metric | Stock/Baseline | After Mod | Date Measured | Notes |
|---|---|---|---|---|
| 0-60 mph | | | | |
| Curb weight | | | | |
| Corner weight (LF/RF/LR/RR) | | | | |
| Skidpad (g) | | | | |
| [Track name] lap time | | | | |

---

## 6. Photo/CAD Log

*Link or embed CAD screenshots, sketches, and photos here as you go. A picture of a hand sketch with reasoning notes on it is genuinely useful — don't wait for polished CAD to start documenting.*

- [ ] [Date] — Initial concept sketch: [description]
- [ ] [Date] — SolidWorks model: [component name]

---

## 7. Open Questions / Research To-Do

*A running list — this is where "I don't know yet" lives, which is honest and normal at this stage.*

- [ ] Confirm actual chassis year/trim once acquired — specs vary by model year
- [ ] Get real corner weights before finalizing spring rates
- [ ] Research [class] rules if entering competition, to avoid designing outside legal limits
- [ ] Learn roll center calculation method before suspension geometry changes

---

## Changelog

| Date | Change |
|---|---|
| [Date] | Document created, initial goals and platform research |
