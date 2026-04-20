[한국어](README.ko.md) | **English**

# Cycling Framework

A data-driven cycling coaching system built on 8 evidence-based frameworks. Routes your training, nutrition, equipment, and event questions to the right expert framework automatically. Powered by Coggan's Power Zones, Friel's Periodization, Seiler's Polarized Training, and more. Built with Korean cyclist context (Zwift/즈위프트, Brevet/브레베, Gran Fondo culture) built in.

> Not medical advice. Consult a sports medicine professional for health concerns.

## Installation

```bash
claude plugin install ironyjk/cycling-framework
```

## Short Command Setup

After installation, add a wrapper command for `/ride`:

```markdown
# ~/.claude/commands/ride.md
---
description: "Cycling coaching — 8 frameworks. Shortcut for /cycling-framework:ride"
---
Invoke the skill `cycling-framework:ride` with these arguments: $ARGUMENTS
```

See the [marketplace wrapper guide](https://github.com/ironyjk/claude-frameworks-marketplace) for details.

## Frameworks

| Command | Framework | Author / Method |
|---------|-----------|-----------------|
| `/ride` | Meta-router | Routes to the best 1–3 sub-frameworks |
| `power-zones` | Power Zone Training | Coggan 7-zone model, FTP, TSS/CTL/ATL/TSB |
| `periodization` | Training Periodization | Friel, linear / block / reverse periodization |
| `polarized-training` | Polarized Training | Seiler 80/20, Z2 base, Zone 5 intervals |
| `nutrition-fueling` | Cycling Nutrition | Carbohydrate loading, in-ride fueling, hydration |
| `bike-fit-equipment` | Bike Fit & Equipment | Saddle height, cleat angle, aero position |
| `indoor-training` | Indoor Training | Zwift (즈위프트), structured workouts, ERG mode |
| `endurance-events` | Endurance Events | Brevet (브레베), Gran Fondo, multi-day preparation |
| `injury-prevention` | Injury Prevention | Overuse injuries, recovery, mobility |

## Usage

```
/ride  I'm training for a 200km brevet in 8 weeks. FTP is 220W, riding 10h/week.
/ride  My knees hurt after every long ride. What's wrong?
/ride  Best nutrition strategy for a 5-hour Gran Fondo?
```

## Attribution & Trademarks

This project implements evidence-based cycling training frameworks for educational purposes. The following trademarks are acknowledged:

- **TrainingPeaks®** and metrics (TSS, CTL, ATL, TSB) are trademarks of TrainingPeaks LLC.
- **Zwift®**, **TrainerRoad®**, **Wahoo KICKR®**, and **Tacx®** are registered trademarks of their respective companies and are referenced as product names only.

All other framework names reference published works and are used descriptively.

This project is not affiliated with, endorsed by, or sponsored by any of the above trademark holders.

## License

[CC-BY-NC 4.0](LICENSE) — Free for personal/educational use. Commercial use requires permission: ironyjk@gmail.com

## Related

- `/fit` ([health-framework](https://github.com/ironyjk/health-framework)) for general fitness, strength, nutrition
- `/think` ([strategy-frameworks](https://github.com/ironyjk/strategy-frameworks)) for decision-making
- [claude-frameworks-marketplace](https://github.com/ironyjk/claude-frameworks-marketplace) — all available frameworks
