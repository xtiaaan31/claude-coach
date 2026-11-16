# Training Load Management

Professional coaches quantify training stress to manage fatigue, prevent overtraining, and peak for races.

## Load Without TSS

TSS is only as good as its inputs. For an athlete without power on the bike or run, or training in heat that inflates heart rate, or who has declined TSS tracking, manage load with three things: weekly planned against actual hours, the weekly share of time in Zones 1–2, and the readiness rules under "Recovery Monitoring". The ramp and recovery-week guidance below still applies, read in hours.

## Training Stress Score (TSS)

TSS measures the physiological cost of a workout. For cycling with power:

```
TSS = (Duration in seconds × NP × IF) / (FTP × 3600) × 100

Where:
- NP = Normalized Power (accounts for variability)
- IF = Intensity Factor (NP / FTP)
```

### TSS Guidelines by Workout Type

| Workout               | Typical TSS | Recovery Needed |
| --------------------- | ----------- | --------------- |
| Easy 1hr ride         | 40-50       | Same day OK     |
| 2hr endurance ride    | 80-100      | 24 hours        |
| Hard interval session | 70-90       | 24-48 hours     |
| 4hr long ride         | 150-200     | 48-72 hours     |
| Century (100mi)       | 250-350     | 3-5 days        |
| Ironman bike          | 300-400     | 1-2 weeks       |

### Running TSS (rTSS)

Estimated from pace and HR. Use Strava's suffer_score as a proxy:

- suffer_score ≈ rTSS for most athletes
- Compare suffer_score per hour across sessions to gauge relative intensity

### Swim TSS (sTSS)

Use duration × intensity factor:

- Easy swim: 25-30 TSS/hour
- Moderate swim: 40-50 TSS/hour
- Hard intervals: 60-70 TSS/hour

---

## Chronic Training Load (CTL) - "Fitness"

CTL is the rolling 42-day weighted average of daily TSS. It represents accumulated fitness.

### CTL Ramp Rate Guidelines

| Athlete Level | Max CTL Increase/Week | Notes                            |
| ------------- | --------------------- | -------------------------------- |
| Beginner      | 3-5 TSS/day           | Conservative to prevent injury   |
| Intermediate  | 5-7 TSS/day           | Standard progression             |
| Advanced      | 7-10 TSS/day          | Aggressive; requires monitoring  |
| Pro           | 8-12 TSS/day          | With careful recovery management |

_A CTL ramp of 7/week means adding ~50 TSS/week to your average weekly load._

---

## Acute Training Load (ATL) - "Fatigue"

ATL is the rolling 7-day weighted average of daily TSS. It represents recent fatigue.

---

## Training Stress Balance (TSB) - "Form"

```
TSB = CTL - ATL
```

| TSB Range  | State        | Implication                                |
| ---------- | ------------ | ------------------------------------------ |
| +15 to +25 | Fresh/peaked | Race ready, may lose fitness if maintained |
| +5 to +15  | Rested       | Good for quality sessions, minor events    |
| -10 to +5  | Neutral      | Normal training state                      |
| -10 to -30 | Fatigued     | Building load, need recovery soon          |
| < -30      | Overreaching | High injury/burnout risk, reduce load      |

### Race Day TSB Targets

| Event       | Target TSB | Taper Length |
| ----------- | ---------- | ------------ |
| Sprint Tri  | 0 to +10   | 5-7 days     |
| Olympic Tri | +5 to +15  | 10-14 days   |
| 70.3        | +10 to +20 | 14-18 days   |
| Ironman     | +15 to +25 | 21-28 days   |
| Marathon    | +10 to +20 | 14-21 days   |

---

## Weekly TSS Targets by Phase

| Phase         | % of Peak TSS | Focus                                  |
| ------------- | ------------- | -------------------------------------- |
| Base (early)  | 60-70%        | Building volume                        |
| Base (late)   | 75-85%        | Volume + introducing intensity         |
| Build         | 90-100%       | Peak volume, race-specific work        |
| Peak          | 85-95%        | Maintaining fitness, sharpening        |
| Taper         | 40-60%        | Reducing volume, maintaining intensity |
| Recovery week | 50-60%        | Every 3-4 weeks                        |

---

## Recovery Monitoring

Readiness works at two speeds. The daily score steers today's session, where acute fatigue is expected. Trends over days and weeks say whether the load itself is right, and belong to the weekly review (`reviews.md`).

The numbers below are defaults. With a coach sheet, a cut-off in `Profile` or an `agreed` row in `Decisions` overrides the default beside it. Evidence label for the daily scheme: coaching judgement, not validated.

### Daily readiness score

**Sleep point** from the watch sleep score: 90–100 → 5, 80–89 → 4, 65–79 → 3, 50–64 → 2, under 50 → 1. Move it by at most 1 toward how the athlete says they slept. With no score, use the athlete's own 1–5.

**Total** = the five scores plus the sleep point (6–30).

| Colour | When                                                                             | Effect on today                                                         |
| ------ | -------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Red    | Total ≤ 14, any score of 1, pain well above usual or sharper, or illness signs   | Quality becomes easy; rest if unwell                                    |
| Amber  | Total 15–19, any score of 2, or pain 1 point above usual                         | Lower half of each target range, fewer reps, one set fewer for strength |
| Green  | Total ≥ 20 and no score below 3; a total of 20–21 works at the bottom of a range | As planned                                                              |

A sleep point of 1 from the watch alone, with the other scores at 3 or more and the athlete feeling fine, is amber.

### Overnight respiratory rate

Against the athlete's baseline (mean and SD in `Profile`; the latest 30 logged nights once there are 30). Label: one coach's experience (Galpin), not research.

- Up to +0.7 breaths/min: no effect.
- +0.8 or more two nights running: at most amber.
- +1.5 or more on one night: at most amber, and ask about illness; with illness signs, red.
- After a night under 5 hours, a raised value reflects the short night: at most amber.
- A normal value never improves the colour.

### Warm-up heart rate

Indoor sessions only, at the fixed warm-up load in `Profile`. Label: coaching judgement.

- Within 4 bpm of normal: keep the plan.
- 5–9 bpm above: drop one level (green → amber, amber → easy).
- 10 or more above, or clearly harder than usual: easy only.
- 5 or more below with breathing or effort harder than usual: drop one level. Lower with normal or easier feel is fitness.

Outdoors in heat, judge by feel and RPE.

### Recovery-week freshness

In recovery weeks, also ask "legs fresh again?" each day until the answer is yes, and log it. The day it turns yes is the athlete's own taper-length evidence.

### Trend indicators

Read these over 3–10 days against the athlete's own baseline, never from a single day. Label: coach's experience (Galpin); the thresholds are rules of thumb.

- **Resting heart rate** is a slow, late marker: 5–10 bpm above baseline for 3 or more days means accumulated fatigue or illness.
- **HRV** moves earlier: a 7-day average 10% or more below baseline means reduce intensity. An athlete whose HRV normally swings widely needs a bigger drop before it means anything.
- **Daily scores:** two or more low scores for 3 or more days means back off; sleep and mood both low is the burnout pattern.
- After 30 logged days, judge each marker against the athlete's own spread: more than 1 SD from the 30-day mean for 3–5 days, or more than 2 SD for two days.
- **Output against HR and feel:** power or pace at the same HR and feel, holding steady or improving, plus mood and still looking forward to training, is the best recovery trend (Bu; coach's experience).
- **Heavy starts:** several sessions in a row that start heavy and only improve as they go, each a little worse, mean the athlete is about to tip over (Bakken; coach's experience). The daily legs score carries it; ask how springy the legs feel on stairs and in the first minutes of sessions.

Before blaming training load for a bad trend, rule out illness, poor sleep, under-fuelling, alcohol and life stress: the body adds them all to one stress total.

### Overreaching

Training load has three outcomes: too little stress gives no adaptation (the most common cause of a plateau); stress above capacity with enough recovery gives adaptation; stress far above capacity, or without recovery, gives a plateau, lost performance and illness or injury risk. A plateau has two opposite fixes, so find which one before acting (Galpin; coach's experience).

| Stage                       | Recovery needed                  | Outcome                                                |
| --------------------------- | -------------------------------- | ------------------------------------------------------ |
| Overload                    | 1–3 days                         | Back better: normal training                           |
| Functional overreaching     | Days to about 2 weeks, less load | Back better: what a block plus recovery week should do |
| Non-functional overreaching | Weeks to months                  | Back to baseline only                                  |
| Overtraining syndrome       | Months or more                   | Rare; more likely in endurance sports                  |

The continuum follows the ECSS/ACSM consensus (Meeusen 2013; research, not re-checked). If a few easy days fix it, it wasn't overtraining.

- **Warning line:** a recovery week that doesn't restore the athlete (still flat, tests down, motivation low) points to non-functional overreaching. Extend easy training, and suggest a doctor to rule out illness before adding load (Claude's judgement).
- **Too little stress** is the first suspect in a plateau. Check that the planned load was actually done before calling it fatigue (`reviews.md`, "Block review").
- **Acute vs chronic fixes:** caffeine, music and a motivating video lift today's session. Sleep, reduced training, more food, social connection and less stress repair accumulated fatigue (Galpin; coach's experience).
- **Recovery extras** (cold or warm baths, massage, rolling) rank far below getting intensity and weekly structure right (Bakken; coach's experience). See `strength.md` for soft-tissue work.
- **Blood markers** are optional. Judge them against the athlete's own baseline, not reference ranges, and only through a doctor.

### Recovery Week Structure

Every 3-4 weeks:

| Day | Prescription                                    |
| --- | ----------------------------------------------- |
| 1   | Complete rest or 30min Zone 1                   |
| 2   | 45-60min Zone 2, single sport                   |
| 3   | 30-45min Zone 2, different sport                |
| 4   | Complete rest                                   |
| 5   | 45-60min Zone 2 with 3-4 short accelerations    |
| 6   | Light session, re-assess readiness              |
| 7   | If feeling good, ease back into normal training |

**Volume reduction:** 40-50% of normal week
**Intensity reduction:** No Zone 4+ work
