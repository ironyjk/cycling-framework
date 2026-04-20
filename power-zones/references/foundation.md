# Power Zone-Based Training (Coggan Power Zones) -- Background & Theory

> This document contains the theoretical foundations, evidence base, and references for this framework.
> For practical application and execution, see [SKILL.md](../SKILL.md).

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


## References

- Coggan, A., Allen, H. *Training and Racing with a Power Meter* (3rd ed., 2019)
- Allen, H. *Power Meter Handbook* (2012)
- Coggan, A. "Power profiling." — TrainingPeaks Blog
- Intervals.icu — Free PMC and power analysis