---
name: indoor-training
version: "0.1.0"
description: "Indoor trainer training — Zwift/TrainerRoad/Wahoo platforms, smart trainer setup, structured workouts, and considerations for Korean apartment environments."
---

# Indoor Trainer Training (Indoor Training)

## One-Line Summary

**Smart trainer + Zwift/TrainerRoad for precise power zone training regardless of weather or time.** Especially useful during Korea's long winters (Nov–Mar) and extreme summer heat (Jul–Aug). Noise and vibration management in apartments is critical.

## Evidence Strength

- Exercise effectiveness of indoor training: **Strong** (same physiological stimulus as outdoor)
- ERG mode accuracy: **Strong** (±1–3W, more consistent than outdoor)
- Zwift virtual racing effectiveness: **Moderate** (motivation + competitive stimulus, but cannot replace outdoor skills)
- Indoor vs outdoor RPE difference: **Strong** (indoor RPE 10–15% higher at same power — impaired heat dissipation)

## Smart Trainer Types

### Direct Drive (Recommended)
- Rear wheel removed; frame mounts directly to trainer
- **Pros**: ±1% accuracy, low noise, stable
- **Recommended**: Wahoo KICKR, Tacx Neo, Elite Suito
- **Price**: 600K–2M KRW (~$450–$1,500)

### Wheel-On (Entry Level)
- Roller contacts the rear tire
- **Pros**: Affordable, easy setup
- **Cons**: Louder, tire wear, ±3–5% accuracy
- **Recommended**: Wahoo KICKR Snap, Tacx Flow
- **Price**: 300K–600K KRW (~$225–$450)

### Rollers (Skill Training)
- Bicycle placed on three rollers; rider maintains balance while pedaling
- **Pros**: Improves balance and pedaling technique, good for warm-ups
- **Cons**: No power control, fall risk, noisy
- **Not recommended for beginners**

## Platform Comparison

| Platform | Monthly Cost | Strengths | Weaknesses |
|---|---|---|---|
| **Zwift** | ~$15 | Virtual world, social, racing | Subscription cost, gamification can be distracting |
| **TrainerRoad** | ~$20 | Structured plans, AI FTP, simple | No visual entertainment |
| **Wahoo SYSTM** | ~$15 | Video + workouts, includes yoga | Small community |
| **Rouvy** | ~$12 | Real-video-based courses | Small user base |
| **Free options** | $0 | TrainingPeaks free + trainer | No visual feedback |

### Zwift Key Features
- **ERG Mode**: Automatically maintains set power (essential for structured workouts)
- **SIM Mode**: Resistance varies with virtual terrain (outdoor feel)
- **Racing**: Real-time virtual races (best for motivation)
- **Workouts**: Hundreds of pre-built workouts + custom creation

## Structured Workouts (Indoor)

### Z2 Base (60–90 min)
```
Warm-up 10 min (Z1→Z2 gradual ramp)
Main set: Z2 steady 40–70 min (ERG mode)
Cool-down 10 min
```
- Can watch Netflix/YouTube during the session
- Watch for cardiac drift: heat accumulation indoors causes HR to rise

### VO2max Norwegian 4×4 (60 min)
```
Warm-up 15 min (Z1→Z2, final 1 min Z4)
4 min Z5 (106–120% FTP) / 3 min Z1 × 4 sets
Cool-down 13 min
```
- ERG mode caution: if cadence drops during Z5, resistance spikes dramatically ("ERG spiral"). Maintaining cadence is critical

### Sweet Spot 2×20 (65 min)
```
Warm-up 15 min
20 min @ 88–94% FTP / 5 min Z1 × 2 sets
Cool-down 10 min
```

### Rønnestad 30/15 (50 min)
```
Warm-up 15 min
30 sec @ 150% FTP / 15 sec Z1 × 13 = 1 set
3 min Z1 recovery × 3 sets
Cool-down 10 min
```

### Short High-Efficiency Session (30 min)
```
Warm-up 5 min
8 min Z4 / 2 min Z1 × 2 sets
Cool-down 5 min
```
- Ideal for time-limited weekday mornings/evenings

## Korean Apartment Environment Considerations

### Noise and Vibration Mitigation
1. **Direct drive trainer** is essential (50%+ less noise than wheel-on)
2. **Trainer mat** (10K–30K KRW / ~$8–$23): absorbs floor vibration + protects from sweat
3. **Additional vibration dampening**: rubber pad or yoga mat layered under the trainer mat
4. **Time restrictions**: avoid before 6 AM or after 10 PM (inter-floor noise regulations, 층간소음)
5. **Placement**: balcony > living room > bedroom (air circulation matters)

### Heat Management (The Biggest Indoor Weakness)
- 30–40% less heat dissipation vs outdoors → HR 10–15 bpm higher at same power
- **Fan is mandatory**: 1–2 large fans, front + side
- **Air conditioning**: combine A/C + fan in summer
- **Hydration**: indoor sweat rate is 1.5× higher → prepare 2+ 500 ml water bottles
- **Towel**: wrap towel around handlebars (prevents sweat corrosion)

### Zwift Setup (Basic)
- Smart trainer + ANT+/Bluetooth connection
- Display: TV/monitor (large screen recommended) or tablet
- Apple TV 4K is the most stable option; PC/Mac also works
- Cadence sensor: not needed if built into the trainer

## Virtual Racing Strategy

### Zwift Race Basics
- **Categories**: A (4.0+ W/kg), B (3.2–4.0), C (2.5–3.2), D (<2.5)
- **First 1–2 minutes**: The hardest segment. Expect 150% of your category's upper W/kg limit
- **Pack drafting**: 25% power savings behind another rider, just like in real life
- **Climbs**: Lighter riders have the advantage. Heavier riders should recover on flats
- **Sprints**: Go all-out in the final 200 m. Timing is everything

## Anti-Patterns

- **Only doing Zwift races** — Racing without structured training means constant Z4–Z5 → overtraining
- **Riding without a fan** — Heat stress causes 20–30% power drop. Training effect also diminishes
- **Ignoring cadence in ERG mode** — Dropping cadence causes resistance to spike → "ERG spiral" trap
- **Indoor training every day** — Mental burnout. 3–4 sessions per week is the upper limit; mix with outdoor
- **Applying outdoor FTP directly to indoor** — Indoor FTP is normally 5–10% lower than outdoor

## Limitations

1. Cannot replace outdoor riding skills (cornering, descending, group riding)
2. Mental boredom and burnout — mitigate with music/video/social features
3. Thermal environment differs from outdoors → outdoor sessions are essential for race preparation
4. Indoor FTP ≠ outdoor FTP (indoor is typically 5–10% lower)

## Complementary Frameworks

- `polarized-training` — Precise 80/20 distribution indoors
- `power-zones` — Accurate zone training via ERG mode
- `periodization` — Leveraging indoor training during winter base periods

## References

- Zwift official documentation (zwift.com)
- TrainerRoad blog — Structured training guides
- DC Rainmaker — Trainer reviews and comparisons
- Minoura, Wahoo, Tacx technical documentation
