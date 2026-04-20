---
name: power-zones
version: "0.2.0"
description: "Power zone-based training — Coggan 7-zone model, FTP testing, TSS/CTL/ATL/TSB fatigue management. The foundation of power meter-driven cycling training."
---

# Power Zone-Based Training (Coggan Power Zones)

> **Background and theory**: Read [references/foundation.md](references/foundation.md)


## One-Line Summary

**Set 7 power zones based on FTP (Functional Threshold Power), and quantitatively manage training load and fatigue with TSS/CTL/ATL/TSB.** The foundation for training design and monitoring for cyclists with a power meter.


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
