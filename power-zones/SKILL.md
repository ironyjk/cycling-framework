---
name: power-zones
version: "0.1.0"
description: "Power zone-based training — Coggan 7-zone model, FTP testing, TSS/CTL/ATL/TSB fatigue management. The foundation of power meter-driven cycling training."
---

# Power Zone-Based Training (Coggan Power Zones)

## One-Line Summary

**Set 7 power zones based on FTP (Functional Threshold Power), and quantitatively manage training load and fatigue with TSS/CTL/ATL/TSB.** The foundation for training design and monitoring for cyclists with a power meter.

## Strength of Evidence

- Coggan 7-zone model: **Strong** (industry standard, adopted by all platforms including TrainingPeaks/Zwift/WKO)
- FTP-based zone setting: **Strong** (high correlation with MLSS)
- TSS/CTL/ATL/TSB model: **Moderate** (convenient but oversimplified; large individual variation)
- 20-minute FTP test ×0.95: **Moderate** (individual variation exists; can overestimate or underestimate)

## Theory & Source References

- **Andrew Coggan, PhD** & **Hunter Allen** — *Training and Racing with a Power Meter* (2006, 3rd ed. 2019)
- **WKO5** — Power duration curve analysis
- **TrainingPeaks** — PMC (Performance Management Chart) system

## 7 Power Zones

| Zone | Name | %FTP | Duration | Purpose | Perceived Effort |
|---|---|---|---|---|---|
| Z1 | Active Recovery | <55% | Unlimited | Recovery | Very easy |
| Z2 | Endurance | 56–75% | 2–6h | Aerobic base | Conversational |
| Z3 | Tempo | 76–90% | 1–3h | Endurance | Short sentences |
| Z4 | Lactate Threshold | 91–105% | 20–60min | FTP improvement | Hard |
| Z5 | VO2max | 106–120% | 3–8min | Maximal oxygen uptake | Very hard |
| Z6 | Anaerobic Capacity | 121–150% | 30s–2min | Anaerobic capacity | Extreme |
| Z7 | Neuromuscular Power | >150% | <15s | Explosive power | All-out |

## FTP Test Protocols

### 20-Minute Test (Most Common)
1. Warm up 20 minutes (Z2 + short accelerations 3×1min)
2. 5-minute all-out effort (clear the legs)
3. 10 minutes easy
4. **20-minute all-out effort** — sustain maximum steady-state power
5. Cool down 10 minutes
6. **FTP = 20-minute average power × 0.95**

### Ramp Test (Simplified)
1. Start at 100W, increase by 20W every minute
2. Continue until failure
3. **FTP = last 1-minute average × 0.75**
- Pros: Simple, less mental burden
- Cons: Overestimates for riders with high anaerobic capacity

### 60-Minute Test (Gold Standard)
- Average power from a 60-minute time trial = FTP
- Most accurate but extremely demanding mentally
- Recommended only for experienced racers

### Testing Frequency
- **Every 4–8 weeks** (or at training block transitions)
- Outdated zone settings lead to inaccurate training intensities
- Test more frequently during rapid fitness changes (return from break, early season)

## W/kg Reference Table

| Level | Male W/kg | Female W/kg | Description |
|---|---|---|---|
| Beginner | 1.5–2.5 | 1.2–2.0 | Less than 1 year of riding |
| Intermediate | 2.5–3.5 | 2.0–3.0 | Consistent training 1–3 years |
| Advanced | 3.5–4.5 | 3.0–3.8 | Structured training 3+ years |
| Elite / Amateur Racer | 4.5–5.5 | 3.8–4.5 | Competitive podium level |
| Professional | 5.5+ | 4.5+ | WorldTour level |

> As body weight decreases, W/kg increases. Combining weight management with FTP improvement yields compounding gains.

## TSS/CTL/ATL/TSB — Training Load Management

### TSS (Training Stress Score)
- **Formula**: TSS = (seconds × NP × IF) / (FTP × 3600) × 100
- **IF** (Intensity Factor) = NP / FTP
- **NP** (Normalized Power) = 4th root of 30-second rolling average
- Rough benchmarks:
  - Z2 for 1 hour ≈ 40–60 TSS
  - Z4 intervals for 1 hour ≈ 70–90 TSS
  - Race for 1 hour ≈ 80–120 TSS

### CTL (Chronic Training Load) — "Fitness"
- 42-day exponentially weighted moving average of daily TSS
- Reflects long-term training adaptation
- Weekly CTL increase target: **3–7 points** (excessive increase = injury risk)

### ATL (Acute Training Load) — "Fatigue"
- 7-day exponentially weighted moving average of daily TSS
- Reflects short-term fatigue accumulation

### TSB (Training Stress Balance) — "Form"
- **TSB = CTL − ATL**
- Positive (+): Well-recovered → race-ready
- Negative (−): Fatigue accumulated → adapting to training
- Race day target: TSB +10 to +25 (peaking)
- Regular training: TSB −10 to −30 (appropriate overload)

### PMC (Performance Management Chart)
```
CTL ──── Gradual upward trend (fitness accumulation)
ATL ──── Rises and falls like waves (training/rest cycles)
TSB ──── Negative when ATL is high, positive after rest
```

## Power Duration Curve (Power Profile)

- Record maximum power at 5-second / 1-minute / 5-minute / 20-minute / 60-minute durations
- Strengths/weaknesses diagnosis:
  - High 5s, low 5min → Sprinter type (criterium strength)
  - High 5min/20min, low 5s → Climber type
  - High 20min/60min, low 5min → Time trialist type
- Auto-analyzed in WKO5 or Intervals.icu

## Practical Considerations

- **Power meter adoption expanding**: Assioma, 4iiii, Stages in the $200–400 range. Best value upgrade available
- **Heart rate monitor only**: Can start with HR zones, but HR has lag and variability, reducing interval accuracy
- **Indoor trainers**: Automatic power measurement on Zwift. ERG mode enables precise zone training
- **Strava/TrainingPeaks/Intervals.icu**: Free-to-paid platforms for PMC management

## Anti-Patterns

- **Setting zones by feel without an FTP test** — Z2 typically set too high (gray zone trap)
- **Always riding Z3–Z4** — "Moderately hard" intensity yields the worst adaptation-to-fatigue ratio
- **Tracking TSS only, ignoring IF** — 100 TSS from a 2-hour Z2 ride and 1-hour Z5 intervals are entirely different
- **Obsessing over CTL numbers** — CTL of 100 is not the goal. Peak CTL matched to your target event is what matters
- **Testing FTP too frequently** — Wastes stress and time. Every 4–8 weeks is appropriate
- **Confusing NP with average power** — On hilly + flat rides, NP >> average. NP more accurately reflects actual physiological load

## Limitations

1. FTP is a single metric — must view 5-second, 1-minute, and 5-minute power alongside it to understand the full profile
2. The TSS model is a simplification — actual fatigue and adaptation vary significantly between individuals
3. Difficult to apply without a power meter — can substitute with HR + RPE but with reduced accuracy
4. FTP is influenced by weather, sleep, nutrition, and stress

## Complementary Frameworks

- `polarized-training` — Time-in-zone distribution strategy
- `periodization` — FTP test timing and zone adjustments within a season
- `recovery-periodization` (`/fit`) — Fatigue management and deload planning

## References

- Coggan, A., Allen, H. *Training and Racing with a Power Meter* (3rd ed., 2019)
- Allen, H. *Power Meter Handbook* (2012)
- Coggan, A. "Power profiling." — TrainingPeaks Blog
- Intervals.icu — Free PMC and power analysis
