---
name: ride
version: "0.3.0"
last_verified: "2026-04-17"
valid_until: "2026-10-17"
description: "Cycling coaching meta-router — 8 evidence-based frameworks (Power Zones/Coggan, Periodization/Friel, Polarized Training/Seiler, Nutrition & Fueling, Bike Fit & Equipment, Indoor Training, Endurance Events, Injury Prevention). Power meter-driven, data-centric training. Built-in context for Korean cyclists. Not medical advice."
tools: ["Read", "Write", "Edit", "Skill", "Agent"]
dependencies:
  - power-zones
  - periodization
  - polarized-training
  - nutrition-fueling
  - bike-fit-equipment
  - indoor-training
  - endurance-events
  - injury-prevention
---

# Cycling Coaching Meta-Router

Classifies cycling training, equipment, and event-related queries, then selects and executes the 1–3 optimal sub-frameworks.

## Detection Matrix

| User Signal | Primary | Secondary |
|---|---|---|
| "FTP", "power zones", "W/kg", "power meter", "TSS" | **power-zones** | polarized-training |
| "season plan", "annual training", "base season", "build phase", "peaking" | **periodization** | power-zones |
| "80/20", "lots of Z2", "ride slow", "LSD", "aerobic base" | **polarized-training** | power-zones |
| "fueling", "gels", "carbs", "how much water", "electrolytes", "weight loss + training" | **nutrition-fueling** | power-zones |
| "saddle height", "fitting", "frame size", "wheels", "tires", "purchase recommendation" | **bike-fit-equipment** | injury-prevention |
| "Zwift", "indoor trainer", "rollers", "Wahoo", "winter training" | **indoor-training** | polarized-training |
| "gran fondo", "century", "brevet", "Seoul–Busan", "Jeju", "long distance" | **endurance-events** | nutrition-fueling / periodization |
| "knee pain", "back", "neck", "hand numbness", "saddle pain", "overtraining" | **injury-prevention** | bike-fit-equipment |
| "just starting", "beginner", "want to buy a road bike", "where do I begin?" | **bike-fit-equipment + power-zones (Starter 2)** | — |
| "race prep", "racing", "criterium" | **periodization + endurance-events** | nutrition-fueling |
| "plateau", "not improving", "FTP stuck" | **polarized-training + power-zones** | periodization |

## Multi-Framework Combinations

| Scenario | Framework Combination |
|---|---|
| **Breaking an FTP Plateau** | power-zones (current analysis) + polarized-training (intensity distribution correction) + periodization (mesocycle adjustment) |
| **First Gran Fondo Preparation** | endurance-events (event plan) + periodization (12–16 week ATP) + nutrition-fueling (fueling strategy) |
| **Winter Off-Season** | indoor-training (structured Zwift) + periodization (Base 1–2) + injury-prevention (off-bike strength) |
| **Weight Loss + Performance** | nutrition-fueling (deficit management) + polarized-training (fat oxidation) + power-zones (W/kg tracking) |
| **Position Discomfort/Pain** | bike-fit-equipment (fit analysis) + injury-prevention (root cause diagnosis) |
| **Full Season Design** | periodization (ATP) + power-zones (zone setup) + polarized-training (intensity distribution) + nutrition-fueling (phase-specific nutrition) |
| **Comprehensive Beginner Guide** | bike-fit-equipment (equipment selection) + power-zones (zone understanding) + polarized-training (basic weekly structure) |

## Goal/Level/Availability Checklist

Confirm or ask before analysis:

- **Goal**: Fitness improvement / FTP increase / Weight loss / Event completion / Race performance / Health maintenance
- **Level**: Beginner (<1 year) / Intermediate (1–3 years) / Advanced (3+ years) / Elite
- **Weekly available hours**: 3h / 5h / 8h / 10h+ — intensity distribution varies accordingly
- **Equipment**: Power meter (yes/no), Indoor trainer (yes/no), Heart rate monitor (yes/no)
- **Current FTP**: If known (W and W/kg)
- **Target event**: Event name, date, distance, elevation
- **Injuries/pre-existing conditions**: Knee, back, neck, other
- **Age/sex**: Affects recovery rate and training volume adjustments

## Korean Cyclist Context

- **Urban riding**: Han River (한강), Tan Creek (탄천), Nakdong River (낙동강), Yeongsan River (영산강), Saejae (새재) — traffic lights and vehicles make Z2 maintenance difficult → early morning/weekends recommended
- **Indoor trainers**: Apartment noise and vibration concerns. Rubber mat + direct-drive trainer recommended. Balcony or dedicated space preferred
- **Summer 35°C+ / Winter below -5°C**: Reduce intensity by 10–15% in extreme temperatures; hydration and electrolyte replenishment essential
- **Gran fondo/brevet culture**: Seoul–Busan (525 km), Jeju circuit (180 km), Yeongju Sobaeksan, Saemangeum, etc.
- **Equipment market**: Giant, Trek, Specialized dealers + online retailers (Biked, Light Bicycle). Used market via Bicycle Market (바이클 마켓)
- **Café ride culture**: Round-trip rides to a destination café serve as training — distinguish between social rides and structured training

## Evidence Strength

- **Strong evidence**: Power zone-based training, polarized 80/20, periodization principles, carbohydrate fueling (60–90 g/h), core strength training
- **Moderate evidence**: Exact accuracy of the 80/20 ratio, HRV-based daily adjustment, ketone adaptation training
- **Weak evidence**: Most supplements (BCAAs, etc.), low-carb performance benefits, specific bike fit "formulas"

## Exclusion Principles

- Doping/drug-related advice
- Medical diagnoses (see a physician first for pain)
- Promotional brand-specific recommendations
- Unrealistic goals such as "increase FTP by 100 W in 3 months"
- Applying professional-level training volume to amateur athletes


## Execution Strategy

1. **Route** -- classify the problem, select 1-3 sub-skills
2. **Confirm** -- verify goal/level/context with the user before analysis
3. **Execute** -- call sub-skills via the Skill tool (read their SKILL.md for execution protocol)
4. **Synthesize** -- combine results, expose conflicts, give concrete next steps
5. **Measure** -- propose 1-2 metrics to track over 4-12 weeks

When a sub-skill needs background theory, read its `references/foundation.md`. Execute using its `SKILL.md`.

## Output Format

```
## Situation Classification
- Goal: [FTP improvement / Weight loss / Event preparation / Health maintenance]
- Level: [Beginner / Intermediate / Advanced]
- Weekly hours: [Xh/week, Y sessions]
- Equipment: [Power meter / Trainer / HR monitor — yes/no]
- Injuries/pre-existing conditions: [List if applicable]

## Selected Frameworks
1. [Framework] — Rationale (evidence strength)
2. ...

## Framework-Specific Analysis
### [Framework 1]
[Analysis results]

## Synthesis
- Points of agreement across frameworks: [Summary]
- Points of conflict: [If any, with rationale and priority]
- Key 1–2 actions for the current phase: [Specific]
- What NOT to do: [Anti-patterns]
- Metrics to track (4–12 weeks): [FTP / Weight / CTL, etc.]

## Safety / Medical
- Hospital first: [Applicable or not]
- Pre-existing conditions/injuries considered: [If any]
```

## Immediate Hospital Escalation

- Chest pain, dyspnea, or syncope during a ride
- Loss of consciousness, severe bleeding, or suspected fracture after a crash
- Sudden severe knee/back pain with radiating pain or numbness
- Headache + nausea + visual disturbance (suspected heat stroke)
- Prolonged loss of sensation in fingers or toes

## Related Domains

- **`/fit`** — General fitness and nutrition management. Particularly linked with `progressive-overload`, `recovery-periodization`, and `macro-tracking`
- **`/learn`** — Leverage `deliberate-practice` and `pomodoro-and-focus` for building training habits
- **`/counsel`** — Sports psychology perspective for race anxiety or motivation issues
