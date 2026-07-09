# Project Civic — Race Car Design Document

- **Author:** [Ryan Spitzmiller]
- **Started:** [July 8th 2026]
- **Status:** [Pre-acquisition planning phase]
- **Platform (candidate):** [1999-2000 DX Honda Civic, EK Chassis, 3-door hatchback]

---

## 1. Project Goals & Requirements

**Primary use case:** [Wheel-to-wheel racing]

**Target sanctioning body:** [SCCA Touring 4 Class]

**Performance targets:**
- Target curb weight: [~2,150-2,250 from 2,359 lbs stock; target strips off ~150-200 lbs from the interior removal, lighter wheels, battery relocation, once cage/safety gear weight accounted for.]
- Target power-to-weight: [TBD]
- Target skidpad / lap time benchmark: [Blackhawk Farms Raceway]

**Budget constraint:** [~$15,000-20,000 over 4-6 years]

**Non-negotiables:** [Prioritization of chassis balance and driver feedback instead of engine power.]

---

## 2. Platform Research & Selection Rationale

| Factor | Spec (stock) | Source |
|---|---|---|
| Curb weight | [2,359 lbs] | [Honda-Tech] |
| Weight distribution (F/R) | [62/38 %] | [Honda-Tech] |
| Wheelbase | [103.2 in] | |
| Track width (F/R) | [58.1 in / 58.1 in] | |
| Suspension type (F) | [Double wishbone] | |
| Suspension type (R) | [Double wishbone] | |
| Engine | [D16Y7, 1.6L, I4] | |
| Stock power/torque | [106 hp / 103 lb-ft] | |
| Drivetrain layout | [FWD] | |

**Why this platform (trade-off reasoning):**
> The EK-chassis DX hatchback shares the double-wishbone front and rear suspension geometry as every other EK trim, meaning it has fundamentally the same handling as the opposing models. Choosing the DX trades horsepower (106 hp D16Y7 vs. 160 hp B16A2) for lower curb weight and lower cost, which fits the project goal of prioritizing chassis balance over raw horsepower. The DX hatchback is chosen over a Miata (common track-build alternative) because of the larger familiarity and aftermarket parts making it cheaper overall build-wise.

**Known weaknesses to design around:**
> As a FWD platform, the DX commonly experiences understeer under power and torque steer during hard acceleration out of corners, which will need to be addressed through front-end grip (tire choice, alignment). The non-VTEC D16Y7 also has a narrower usable power band than VTEC engines, which affect gear ratio choices for Touring 4.

---

## 3. Subsystem Design Log

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
