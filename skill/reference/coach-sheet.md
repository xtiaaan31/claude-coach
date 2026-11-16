# Coach Sheet

The coach sheet is a Google spreadsheet used as the coach's database. It holds the living plan and everything the coach remembers between conversations. Every fact about the athlete lives here; the skill files hold only the method.

Read and write it through the Google Sheets connector. The athlete gives the spreadsheet link (in the scheduled task prompt, in project instructions, or when asked). When no link is in context, ask for one.

## Table rules

Each tab below is a table: row 1 is the header, every later row is one record.

- Find a column by its header text, so the athlete can reorder or add columns.
- Dates are `YYYY-MM-DD`. Durations are whole minutes. One value per cell, plain text or number, typed (no formulas, no merged cells).
- Change a record by updating its row. Add a record by appending a row. Log tabs (`Check-ins`, `Tests`, `Decisions`) are append-only: a correction is a new row.
- Other tabs in the spreadsheet belong to the athlete. Read them when asked; write only to the six tables.

When a table is missing, create it with the header below and tell the athlete.

## Sessions

One row per planned session. This table is the plan.

| Column      | Contents                                                                                          |
| ----------- | ------------------------------------------------------------------------------------------------- |
| ID          | `YYYY-MM-DD-sport`, with `-2` for a second session of that sport that day                         |
| Date        | Day of the session                                                                                |
| Week        | Monday of that week (joins to `Weeks`)                                                            |
| Sport       | Swim, Bike, Run, Strength, Other                                                                  |
| Code        | Workout library code (see `workouts.md`), or a short name for sessions outside the library        |
| Session     | Every step with its target (zone plus the athlete's own number), fuelling and gates included      |
| Planned min | Whole session, warm-up and cool-down included; the steps in `Session` add up to it                |
| Status      | planned, done, changed, skipped                                                                   |
| Actual min  | From the recorded activity                                                                        |
| RPE         | Athlete's 1–10 for the session                                                                    |
| Notes       | What the athlete said about it (pain, heat, feel)                                                 |
| Activity ID | Strava activity ID once matched; several, comma-separated, when one session was recorded in parts |
| Review      | The coach's one-line verdict: executed as planned or not, and the one thing that matters next     |

`changed` means the session was done differently from the row as first agreed; put what changed and why in `Review`.

## Weeks

One row per week of the season. This table is the annual plan.

| Column          | Contents                                                              |
| --------------- | --------------------------------------------------------------------- |
| Week            | Monday of the week                                                    |
| Target          | The race this block builds to                                         |
| Period          | Prep, Base 1–3, Build 1–2, Peak, Race, Transition                     |
| Type            | load, recovery, test, taper, race                                     |
| Planned h       | Endurance hours planned                                               |
| Strength phase  | AA, MT, MS, SM, none                                                  |
| Abilities       | The abilities trained that week (see `periodization.md`)              |
| Actual h        | Filled by the weekly review                                           |
| Easy %          | Share of actual time in Zones 1–2, filled by the weekly review        |
| Looking forward | The athlete's y/n answer to "still looking forward to training?"      |
| Review          | The weekly review's summary and what it changed for the week after it |

## Check-ins

One row per morning. Append-only.

| Column     | Contents                                                                |
| ---------- | ----------------------------------------------------------------------- |
| Date       | Morning of the check-in                                                 |
| Sleep      | Watch sleep score, or blank                                             |
| Resp rate  | Overnight breaths per minute, or blank                                  |
| Energy     | 1–5, 5 is best                                                          |
| Legs       | 1–5                                                                     |
| Stress     | 1–5                                                                     |
| Mood       | 1–5                                                                     |
| Motivation | 1–5                                                                     |
| Sleep pt   | The sleep score converted to 1–5                                        |
| Total      | Sum of the five scores and the sleep point                              |
| Pain       | 0–10 for the athlete's tracked pain site (named in `Profile`)           |
| Illness    | Signs the athlete reports, or blank                                     |
| Colour     | green, amber, red                                                       |
| Warm-up HR | Heart rate at the fixed warm-up load, and its difference from normal    |
| Fresh legs | Recovery weeks only: y/n to "legs fresh again?"                         |
| Change     | What was changed in today's session, or "none"                          |
| Note       | Anything else worth reading back in a month (short night, travel, heat) |

## Tests

One row per test. Append-only. The latest row per sport sets the current zones.

| Column     | Contents                                                |
| ---------- | ------------------------------------------------------- |
| Date       | Day of the test                                         |
| Sport      | Swim, Bike, Run, Strength, Other                        |
| Protocol   | The exact test, so later results compare like with like |
| Result     | The raw result (time, average power, average HR)        |
| Threshold  | The value derived from it (CSS, FTP, LTHR)              |
| Zones      | Zones 1–5 as ranges, computed per `zones.md`            |
| Conditions | Indoor or outdoor, heat, fatigue, anything that skews   |
| Note       | How it compares with the previous test                  |

## Decisions

One row per decision. Append-only. Read the whole table before proposing anything.

| Column   | Contents                                                           |
| -------- | ------------------------------------------------------------------ |
| Date     | Day it was decided                                                 |
| Topic    | Strength, Run, Fuelling, Monitoring, …                             |
| Decision | What was agreed or declined, as a rule the coach can apply         |
| Reason   | Why, with the source and its evidence label                        |
| Status   | agreed, declined, superseded                                       |
| Replaces | The date and topic of the row this one supersedes, when it has one |

A `declined` row is a standing preference: leave that idea alone unless the athlete raises it or new data from the athlete gives a reason, and say which data.

## Profile

One row per fact about the athlete, as `Key`, `Value`, `Updated`, `Note`. The first run asks for the facts that are missing. Expected keys:

| Key                | Value                                                                                 |
| ------------------ | ------------------------------------------------------------------------------------- |
| Check-in time      | Local time and timezone of the daily check-in, chosen by the athlete                  |
| Units              | Metric or imperial, per sport if they differ                                          |
| Races              | Each race with date, distance and priority (A, B, C)                                  |
| Weekly template    | Which sport and session type falls on which day, and what is indoor or outdoor        |
| Equipment          | Bike, trainer, power meters, watch, HR strap, treadmill, pool length                  |
| Pain site          | The site the `Pain` score tracks and its usual value                                  |
| Injury patterns    | Known recurring issues and their early warning signs                                  |
| Readiness cut-offs | Any cut-off that differs from the defaults in `load-management.md`                    |
| Resp baseline      | Mean and SD of overnight respiratory rate, and the nights it covers                   |
| Warm-up normal     | Per indoor sport: the fixed warm-up load and the normal HR at it                      |
| Test protocols     | The protocol used per sport                                                           |
| Health data        | Link and column map of the athlete's health export, and whether it is kept up to date |
| Preferences        | Standing preferences that are not decisions about one topic                           |

## Plan view

The sheet is the source of truth; an HTML page is a view built from it. Build one when the athlete asks and after each weekly review:

- **With a shell (Claude Code):** write the `Weeks` and `Sessions` rows as TrainingPlan JSON and run `npx claude-coach render` (see "Plan Output Format" in `SKILL.md`).
- **Without a shell:** build an HTML page directly from the rows, showing today, the current week by day, and the season by week.

State on the page the date and time it was built.
