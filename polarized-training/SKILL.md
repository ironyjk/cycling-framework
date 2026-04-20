---
name: polarized-training
version: "0.2.0"
description: "Cycling-specific polarized training — applying Seiler's 80/20 principle to cycling. Weekly training plans, indoor trainer workouts, and integration with Friel periodization."
---

# Polarized Training — Cycling-Specific

> **Background and theory**: Read [references/foundation.md](references/foundation.md)


## One-Line Summary

**Allocate 80% of training time to Z1–Z2 (easy intensity) and 20% to Z4–Z5 (high intensity). Minimize Z3 (moderate intensity).** Provides cycling-specific, actionable plans beyond the general `polarized-endurance` framework in `/fit`.


## Weekly Plans (By Volume)

### 4–5 Hours/Week (Minimum Effective Dose)
```
Mon: Rest
Tue: Z5 intervals 50min (5×4min @106–120%FTP / 3min Z1)
Wed: Rest or Z1 30min
Thu: Z2 60min
Fri: Rest
Sat: Long Z2 2–2.5h
Sun: Z2 60min
```
→ Low ~80%, High ~20% | Weekly TSS ~250–300

### 6–8 Hours/Week (Amateur Standard)
```
Mon: Rest
Tue: Z2 90min
Wed: Z5 intervals 70min (4×4min @Z5 + 2×8min @Z4)
Thu: Z2 60min (recovery)
Fri: Z5 intervals 60min (Rønnestad 30/15 × 3 sets)
Sat: Long Z2 3–4h
Sun: Z2 60–90min
```
→ Low ~80%, High ~18% | Weekly TSS ~400–550

### 10+ Hours/Week (Dedicated Amateur)
```
Mon: Rest
Tue: Z2 90min
Wed: Z5 intervals 75min (5×4min Norwegian)
Thu: Z2 90min
Fri: Z4/Z5 mixed 70min (3×12min @Z4 + 3×3min @Z5)
Sat: Long Z2 4–5h
Sun: Z2 90min + optional Z3 block 20min
```
→ Low ~82%, High ~15% | Weekly TSS ~600–750


## Key High-Intensity Workouts

### 1. Norwegian 4×4 (VO2max Gold Standard)
- 4min @Z5 (106–120% FTP) / 3min Z1 recovery × 4 sets
- Total 28min of work
- Goal: VO2max stimulus. HR approaches max by the 4th minute
- 1–2 times per week

### 2. Rønnestad 30/15 (Short Intervals)
- 30sec @150–170% FTP / 15sec Z1 × 13 reps = 1 set (9.75min)
- 3min recovery, repeat × 3 sets
- Total ~35min of work
- Simultaneous anaerobic + aerobic stimulus. Caution: extremely demanding

### 3. Sweet Spot Intervals (Caution: Gray Zone Boundary)
- 12–20min @88–94% FTP × 2–3 sets
- From a polarized perspective, this is an "ambiguous zone"
- **When to use**: As a transition between Z4 and Z2 during the Build period. Do not use weekly

### 4. Over-Under (Threshold Adaptation)
- 2min @Z4 (95–105%) + 1min @Z5 (110–115%) repeated × 8–10
- Tolerance training near threshold
- Best suited for the Build 2 period


## Integration with Friel Periodization

| Periodization Phase | Polarized Application |
|---|---|
| Base 1–2 | **90/10**: Nearly all Z2. Minimal high intensity (optional 1× short Z5 per week) |
| Base 3 | **85/15**: Begin introducing Z4 |
| Build 1 | **80/20**: 2× high intensity per week (primarily Z4) |
| Build 2 | **75/25**: Increased Z5 proportion, race simulations |
| Peak | **85/15**: Reduced volume, maintain stimulus with short high-intensity efforts |
| Transition | **100/0**: Ride freely |


## Indoor Trainer Utilization

The **indoor trainer is a powerful tool** for polarized training:
- ERG mode: Maintains precise power zones (precision impossible outdoors)
- Z2 training: Uninterrupted continuous Z2 without traffic lights or vehicles
- VO2max intervals: Exact power targets, safe environment

### Recommended Zwift Workouts
- **Z2 Base**: "Foundation" or custom fixed Z2
- **VO2max**: "The Gorby" (4×4min), "The McCarthy Special"
- **30/15**: TrainerRoad "Baird" or custom


## Practical Realities for Korean Cyclists

- **Difficulty maintaining Z2 on the Han River path**: Crowded bike lanes, traffic signals, pedestrians → early morning (5–6 AM) or head toward Paldang–Yangpyeong
- **Group ride dilemma**: Most club rides sit in Z3 (gray zone). Separate social rides from structured training
- **"Riding slow is embarrassing"**: In Korean cycling culture, Z2 = slow = weak. However, even pros spend 80% in Z2
- **Limited weekday time**: 1–1.5 hours before/after work → high intensity on Tue/Thu, Long Z2 on weekends


## Anti-Patterns

- **Chasing Strava KOMs on every ride** — Tempted by segment records during Z2 rides → drifting into Z3–Z4
- **Ignoring "easy days should be easy"** — Moderate intensity every day = chronic fatigue
- **VO2 sessions 3+ times per week** — Immune suppression, fatigue accumulation. 2× per week is the upper limit
- **Polarized training without a power meter** — Possible with HR, but interval precision suffers
- **Mistaking group rides for Z2** — A group averaging 30 km/h is almost always Z3+


## Limitations

1. **Under 3 hours/week**: Threshold-focused training may be more time-efficient than polarized
2. **Individual response variance**: Some athletes may respond better to a Sweet Spot-focused approach
3. **Exact 80/20 doesn't matter**: Anywhere within 75–90/10–25 is sufficient
4. **Boredom**: Z2-dominant training is mentally challenging → leverage podcasts, movies, Zwift


## Complementary Frameworks

- `power-zones` — Foundation for zone configuration
- `periodization` — Adjusting the 80/20 ratio by training phase
- `indoor-training` — Precision execution environment for polarized training
