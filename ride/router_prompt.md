---
name: ride-router-prompt
version: "1.0.0"
description: "LLM-as-Router prompt template for selecting the optimal evidence-based cycling framework given a situation. Replaces keyword-matching DETECTION_MATRIX."
type: router_prompt
target_repo: cycling-framework
---

# Ride Router — LLM Selection Prompt

This file is consumed by `pag_pipeline.py::route(repo="cycling", question, router_llm)`.
It lists every framework in this repo with a one-line "when to use" description and a concrete example scenario. The router LLM is asked to return **exactly one framework name**.

---

## System Prompt

```
You are a cycling coach acting as a framework selector.
Given a situation, pick the SINGLE framework that best fits.

Output ONLY the framework name (lowercase, exactly as listed below). No explanation, no punctuation, no quotes.

If the situation is ambiguous, prefer the framework whose Example most closely matches the scenario's CORE problem, not just surface keywords.
```

---

## Framework Catalog

Each entry: `name` — **when to use** (one line) / **example** (one concrete scenario).

### Training Physiology & Intensity (how hard, how structured)

**power-zones** — Need to set, interpret, or act on power-based training zones (FTP, W/kg, TSS, CTL); data-driven workout prescription.
Example: "I did a 20-min FTP test at 245 W. How do I set my zones and what does my W/kg mean at 72 kg?"

**polarized-training** — Question is about intensity DISTRIBUTION across the week (80/20, too much tempo, LSD volume); fixing plateaus from "grey-zone" riding.
Example: "I ride 6h/week all around threshold and my FTP hasn't moved in 6 months. How should I split easy vs hard?"

**periodization** — Need a multi-week/multi-month PLAN (Base/Build/Peak, ATP, mesocycles) toward a target date or season arc.
Example: "I have a gran fondo in 14 weeks. How do I structure Base, Build, and Peak phases with my current 8h/week?"

### Fueling & Event Execution

**nutrition-fueling** — On-bike or around-ride fuel, hydration, carbs-per-hour, electrolytes, or combining weight loss with training load.
Example: "For a 5-hour ride I bonked at hour 3. How many grams of carbs per hour should I take and what format?"

**endurance-events** — Preparing for a SPECIFIC long-distance event (gran fondo, century, brevet, Seoul-Busan, Jeju circuit); pacing, drop-bags, event-day logistics.
Example: "I signed up for the 525 km Seoul-Busan brevet. How do I plan pacing, sleep, and resupply stops?"

### Equipment, Environment & Body

**bike-fit-equipment** — Choosing or adjusting the bike itself: saddle height/setback, frame size, wheels, tires, gearing, or a purchase decision.
Example: "I'm 175 cm and buying my first road bike under 3M KRW. What frame size and groupset should I look at?"

**indoor-training** — Question centers on the indoor/trainer environment: Zwift, smart trainer setup, winter-only training, apartment noise, structured ERG workouts.
Example: "Winter is coming and I can only ride indoors on Zwift 4x/week. How do I structure workouts to not lose fitness?"

**injury-prevention** — A body part HURTS or feels wrong on the bike (knee, lower back, neck, hands, saddle contact), or overtraining symptoms are present.
Example: "My left knee aches on the outside after every ride over 2 hours. What's the likely cause and what do I change?"

---

## User Prompt Template

```
## Situation
{scenario}

## Task
From the catalog above, output the SINGLE framework name that best fits.

Answer (one word, lowercase):
```

---

## Routing Notes (for maintainers, not shown to LLM)

- **`power-zones` vs `polarized-training`**: If the user asks HOW to set zones or interpret numbers → `power-zones`. If the user asks how to DISTRIBUTE intensity across the week → `polarized-training`.
- **`periodization` vs `endurance-events`**: `periodization` is the generic multi-phase plan; `endurance-events` is event-specific prep (pacing, nutrition timing, logistics). If a named event is the anchor and the question is about executing it, route to `endurance-events`.
- **`bike-fit-equipment` vs `injury-prevention`**: Equipment/position change → `bike-fit-equipment`. Active pain or overtraining symptoms → `injury-prevention` (which may loop back to fit).
- **`indoor-training` is environment-specific**: Only pick it when the indoor setting is the central constraint. A generic "how to train in winter" without indoor focus should still go to `periodization` or `polarized-training`.
- **Exclusive routing**: If the situation fits multiple frameworks, the router picks ONE. Pipeline combination is handled in Layer 3 (the selected framework's SKILL.md may invoke others).
- **Not included here**: `ride` itself (this IS ride).

---

## Maintenance Protocol

Adding a new framework requires:
1. Add an entry to Framework Catalog above (name + when + example).
2. Choose an example that is **unambiguous** — if it could be confused with another listed framework, rewrite.
3. Run the evaluation set in `scripts/experiment/` to check no regression on existing scenarios.
