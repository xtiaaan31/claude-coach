# Reviews

The plan is fluid: it is re-decided at four rhythms as the athlete responds. Each review has its own inputs and its own **reach**, the furthest part of the plan it may change. A review that sees a problem beyond its reach names it and leaves it to the review that owns it.

| Review | Runs                                                 | Reach                               |
| ------ | ---------------------------------------------------- | ----------------------------------- |
| Daily  | Each morning at the athlete's check-in time          | Today and tomorrow                  |
| Weekly | With the first check-in of the week                  | The week ahead                      |
| Block  | When a recovery or test week closes, results in hand | Zones and the next block            |
| Season | After each A race and at the season break            | The annual plan (the `Weeks` table) |

Any review also runs when the athlete asks for it.

All four read and write the coach sheet (`coach-sheet.md`). Recorded activities come from the Strava connector when its tools are present, otherwise from the local database (`queries.md`).

## Authority

The athlete owns the plan. The coach proposes; a change is written to the sheet after the athlete agrees. Each proposal states what changes, the data behind it, and the evidence label of the rule it rests on.

One exception: a same-day swap under a rule already in force (the readiness rules below, or an `agreed` row in `Decisions`) is applied at once and reported in the same message.

Every agreement or refusal that should hold beyond today becomes a `Decisions` row. Read `Decisions` and `Profile` before proposing: an `agreed` row is a rule, a `declined` row is settled.

## Daily review

1. **Post the day.** Read today's `Sessions` rows. Find yesterday's activities and match each to its row. For today's indoor sessions, give the normal warm-up heart rate from `Profile`. Ask for the check-in.
2. **Take the check-in.** The athlete replies with the sleep score, overnight respiratory rate, five 1–5 scores (energy, legs, stress, mood, motivation), the pain score and any illness signs. Ask once for anything missing that the rules need.
3. **Set the colour** with the readiness rules below.
4. **Adjust today** by the colour, and tomorrow only when today's change moves a quality session onto it.
5. **Review yesterday.** For each matched activity, compare what was done with the row's steps and targets: time in the prescribed zone, drift above the easy ceiling, reps hit or missed, RPE against the intended effort. Read the per-second streams for quality sessions and for any session the athlete flagged.
6. **Write the rows.** Append the `Check-ins` row. Update yesterday's `Sessions` rows (status, actual minutes, RPE, notes, activity ID, review) and today's rows if they changed.

Done when today's `Check-ins` row exists and every session of yesterday has a status and a review line.

### Readiness rules

These are the defaults. A cut-off in `Profile` overrides the default beside it. Evidence label for the whole scheme: coaching judgement, not validated. Its purpose is to steer today's session; acute fatigue is expected, and trends are the weekly review's business.

**Sleep point** from the watch sleep score: 90–100 → 5, 80–89 → 4, 65–79 → 3, 50–64 → 2, under 50 → 1. Move it by at most 1 toward how the athlete says they slept. With no score, use the athlete's own 1–5.

**Total** = the five scores plus the sleep point (6–30).

| Colour | When                                                                             | Effect on today                                                         |
| ------ | -------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Red    | Total ≤ 14, any score of 1, pain well above usual or sharper, or illness signs   | Quality becomes easy; rest if unwell                                    |
| Amber  | Total 15–19, any score of 2, or pain 1 point above usual                         | Lower half of each target range, fewer reps, one set fewer for strength |
| Green  | Total ≥ 20 and no score below 3; a total of 20–21 works at the bottom of a range | As planned                                                              |

A sleep point of 1 from the watch alone, with the other scores at 3 or more and the athlete feeling fine, is amber.

**Respiratory rate** against the athlete's baseline (mean and SD in `Profile`; the latest 30 logged nights once there are 30). Label: one coach's experience (Galpin), not research.

- Up to +0.7 breaths/min: no effect.
- +0.8 or more two nights running: at most amber.
- +1.5 or more on one night: at most amber, and ask about illness; with illness signs, red.
- After a night under 5 hours, a raised value reflects the short night: at most amber.
- A normal value never improves the colour.

**Warm-up heart rate**, indoor sessions only, at the fixed warm-up load in `Profile`. Label: coaching judgement.

- Within 4 bpm of normal: keep the plan.
- 5–9 bpm above: drop one level (green → amber, amber → easy).
- 10 or more above, or clearly harder than usual: easy only.
- 5 or more below with breathing or effort harder than usual: drop one level. Lower with normal or easier feel is fitness.

Outdoors in heat, judge by feel and RPE.

In recovery weeks, also ask "legs fresh again?" each day until the answer is yes, and log it. The day it turns yes is the athlete's own taper-length evidence.

## Weekly review

1. **Close last week.** Sum actual hours per sport against planned. Compute the share of time in Zones 1–2. List sessions skipped, changed or cut short.
2. **Read the trends** across the week's `Check-ins`: colours, pain scores, warm-up heart rate against normal, respiratory rate. Ask "still looking forward to training?" When the athlete's health export is up to date (`Profile`), read resting heart rate and HRV as a trend over 3–10 days, never a single day.
3. **Judge the response.** Flags: three or more sessions with warm-up heart rate 5+ bpm off normal, pain trending up, a second "no" in a row to looking forward, easy share under the plan's target, hours well under plan two weeks running. Before blaming training load, rule out illness, poor sleep, under-fuelling, alcohol and life stress.
4. **Propose the week ahead.** With no flags, the week stands. With flags, propose the smallest change that answers them: cap quality, repeat last week's load, or pull the recovery week forward.
5. **Write the rows.** Fill last week's `Weeks` row. Update the coming week's `Sessions` rows for what was agreed. Rebuild the plan view.

Done when last week's `Weeks` row is filled and every flag has either an agreed change or the athlete's decision to leave the week as it is.

## Block review

1. **Record the tests.** Append a `Tests` row per test with the protocol named exactly. Compute new zones per `zones.md`.
2. **Compare.** Each result against the previous one under the same protocol and against what the block set out to train. Read the result as a band: heat, fatigue and fuelling move it.
3. **Explain a stall before changing the plan**, in this order: health and life stress; whether the planned load was actually done (hours, easy sessions truly easy, quality reps hit); only then the training itself.
4. **Write the next block.** Take the block's weeks from `Weeks`, build its sessions (`periodization.md`, `workouts.md`), with targets from the new zones, and present it for agreement. Rescale any already-written future sessions to the new zones.
5. **Update the baselines** in `Profile` that this block's data moved: respiratory-rate baseline, warm-up normal, usual pain score.

Done when the new zones are in `Tests`, every future `Sessions` row uses them, and the next block's rows are agreed and written.

## Season review

1. **Race against plan.** Splits, pacing, fuelling and conditions against the race plan (`race-day.md`), and the athlete's own account.
2. **Season against last season.** From `Tests`, `Weeks` and `Check-ins`: threshold changes per sport, hours done against planned, weeks lost and why, which blocks produced the gains, how long the taper took to feel fresh.
3. **Name the limiter** for the next block or season, and what the data says the athlete responds to.
4. **Propose the annual plan** for what comes next: races, periods, weekly hours, recovery pattern. After agreement, write the `Weeks` rows.
5. **Review the standing rules.** Read `Decisions` and `Profile` with the athlete: which rules still hold, which the season's data argues against. The season break is the moment to change a test protocol.

Done when the `Weeks` table covers the period up to the next A race and the athlete has confirmed the rules carried forward.
