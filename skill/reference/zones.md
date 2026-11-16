# Training Zones & Field Testing

Professional coaching requires accurate training zones derived from field tests, not arbitrary percentages of max HR.

## 80/20 Zones

Sessions taken from the 80/20 Workout Library (`workouts.md`) use 80/20's zones. In those sessions, "Zone 3" means 80/20 Zone 3, not Friel's. Zones X and Y are the gaps between zones. They aren't training targets: drifting into one means the session missed its zone.

| Zone | Plan word | Run, % of LTHR | Bike, % of FTP | Swim, % of threshold speed |
| ---- | --------- | -------------- | -------------- | -------------------------- |
| 1    | very easy | under 81       | 50–70          | 75–84                      |
| 2    | easy      | 81–89          | 70–83          | 84–91                      |
| X    | avoid     | 90–95          | 83–91          | 91–96                      |
| 3    | threshold | 96–100         | 91–100         | 96–100                     |
| Y    | avoid     | 101–102        | 100–102        | 100–102                    |
| 4    | hard      | 103–105        | 102–110        | 102–106                    |
| 5    | hard      | 106 and up     | over 110       | over 106                   |

The bike column was checked against 80/20's intensity pages in November 2026 (research). The run and swim columns are back-calculated from 80/20 zone-calculator output (not checked against the page). Use 80/20's calculator when it disagrees.

- **Swim pace from speed:** zone pace = threshold pace ÷ (% of speed). At a 2:00/100 m threshold, 90% speed is 2:13/100 m. Pace-based and speed-based percentages diverge at easy intensities, so never take a percentage of pace directly.
- **Easy means below the first threshold.** Zones 1–2 sit below LT1 (Seiler; research). For easy sessions the ceiling matters more than the floor. Sliding into high Zone 1 on a hot day is fine; sliding into X is the common failure.
- **Rough mapping to Friel's zones:** 80/20 Zones 1–2 ≈ Friel 1–2; X ≈ Friel 3 (tempo); 80/20 Zone 3 ≈ Friel 4 to 5a; Zone 4 ≈ 5b; Zone 5 ≈ 5c. Use one system per plan.
- **When X has a job:** for half and full Ironman athletes, race intensity falls in or near X. In the last 12 weeks, 80/20 adds a small dose of race-pace work there (see "Race-specific phase" in `periodization.md`). Outside that, X stays a gap.

## Lactate Threshold Heart Rate (LTHR) Zones

LTHR is the heart rate at lactate threshold—the intensity you could sustain for approximately 60 minutes in a race. It's more accurate than max HR for prescribing training.

### Running LTHR Zones (Friel 7-Zone System)

| Zone | Name          | % of LTHR | Purpose                                | Feel                               |
| ---- | ------------- | --------- | -------------------------------------- | ---------------------------------- |
| 1    | Recovery      | < 81%     | Active recovery, warm-up/cool-down     | Very easy, could talk indefinitely |
| 2    | Aerobic       | 81-89%    | Aerobic base building, fat oxidation   | Easy, full conversations           |
| 3    | Tempo         | 90-93%    | Muscular endurance, aerobic capacity   | Moderate, sentences only           |
| 4    | Sub-threshold | 94-99%    | Lactate tolerance, threshold extension | Hard, few words at a time          |
| 5a   | Threshold     | 100-102%  | Lactate threshold improvement          | Very hard, race effort for 60min   |
| 5b   | VO2max        | 103-106%  | VO2max development                     | Extremely hard, 3-8min max         |
| 5c   | Anaerobic     | > 106%    | Neuromuscular power, speed             | Max effort, < 3min                 |

### Cycling LTHR/Power Zones

| Zone | Name          | % of LTHR | % of FTP | Purpose             |
| ---- | ------------- | --------- | -------- | ------------------- |
| 1    | Recovery      | < 81%     | < 55%    | Active recovery     |
| 2    | Aerobic       | 81-89%    | 56-75%   | Endurance base      |
| 3    | Tempo         | 90-93%    | 76-90%   | Muscular endurance  |
| 4    | Sub-threshold | 94-99%    | 91-99%   | Threshold extension |
| 5a   | Threshold     | 100-102%  | 100-105% | FTP improvement     |
| 5b   | VO2max        | 103-106%  | 106-120% | VO2max intervals    |
| 5c   | Anaerobic     | > 106%    | > 120%   | Neuromuscular power |

### Swimming Zones (CSS-based)

| Zone | Name      | Pace Relative to CSS | Purpose               |
| ---- | --------- | -------------------- | --------------------- |
| 1    | Recovery  | CSS + 15-20 sec/100m | Warm-up, cool-down    |
| 2    | Aerobic   | CSS + 8-12 sec/100m  | Aerobic endurance     |
| 3    | Tempo     | CSS + 3-6 sec/100m   | Lactate tolerance     |
| 4    | Threshold | CSS pace             | Threshold development |
| 5    | VO2max    | CSS - 3-5 sec/100m   | VO2max intervals      |

---

## Field Testing Protocols

### Run: 30-Minute Threshold Test

1. Warm up 15 minutes easy (Zone 1-2)
2. Run 30 minutes at the hardest sustainable pace (simulate race effort)
3. Record average HR for the entire 30 minutes = LTHR
4. Cool down 10 minutes easy
5. Average pace = approximate lactate threshold pace

_Note: Some coaches use final 20 minutes of a 30-min test to exclude early pacing errors._

### Bike: 20-Minute FTP Test

1. Warm up 20 minutes including 3x1min high-cadence spin-ups
2. Ride 20 minutes at maximum sustainable power
3. Average power × 0.95 = FTP
4. Average HR = approximate cycling LTHR
5. Cool down 10-15 minutes

_Alternative: 2x8 minute test with 10min recovery; average power × 0.90 = FTP_

### Swim: Critical Swim Speed (CSS) Test

1. Warm up 400m easy with drills
2. Swim 400m time trial (all-out, record time)
3. Rest 10 minutes (active recovery)
4. Swim 200m time trial (all-out, record time)
5. CSS = (400m distance - 200m distance) / (400m time - 200m time)

_Example: 400m in 6:40 (400 sec), 200m in 3:00 (180 sec)_
_CSS = 200m / 220 sec = 0.909 m/sec = 1:50/100m_

### 80/20 Test Versions

- **Run, 80/20 LTHR time trial:** after the warm-up, run the hardest effort you can hold for 20 minutes, with a lap at 5 minutes. LTHR is the average HR of the last 15 minutes. Hold back slightly in the first 5. 80/20 notes that LTHR is specific to the conditions of the test, so test where the key runs happen (research: 80/20 help centre).
- **Swim, STT2:** 200 Zone 1, 400 all-out, 2 min rest, 200 all-out, 2 min rest, 200 Zone 1. CSS is computed from the 400 and 200 as above. The library labels the two swims Zone 3. Swim them all-out, because CSS needs maximal efforts.
- **Bike:** the library has no cycling test. Use the 20-minute FTP test above.

### Same Conditions Every Time

A test only compares with an earlier one under the same protocol and conditions (Galpin, "bad data is worse than no data"; coach's experience). Fix:

- place, surface and time of day
- warm-up, including any surges in it
- shoes, bike setup and fan
- fuelling before the test, and the 48 hours before it

Record anything that differs in the `Tests` row's Conditions column. Name the protocol exactly. When a protocol changes, the next test starts a new series and can't be compared with the old one.

Plan tests in recovery weeks, when the athlete is fresh. Move a test rather than run it sick or just after an illness, because the result would set zones too low.

### Reading a Test

- **A threshold is a band, not a line.** Heat, accumulated fatigue, low carbohydrate and long efforts beforehand all lower it. One all-out 3-minute effort can cut critical power by about 7%, and 2 hours of heavy riding by about 9% (critical-power researchers on That Triathlon Show; not checked). Start threshold sessions at the low end of Zone 3 and build only if it feels sustainable. Read a retest that comes in a little lower on a hot day as noise, not lost fitness.
- **FTP vs critical power:** in triathletes the two usually agree (Eriksson; coach's experience). A 3-trial CP test costs more recovery than one 20-minute test. Keep whichever protocol the athlete already uses.
- **What a test reflects:** a retest 3–4 weeks into a block mostly shows the quality sessions and recovery from any recent illness. Gains from added easy volume take 2–3 months to show (That Triathlon Show hosts on a 6-week study; coach's experience). Judge volume at the later retests.
- **Early gains, later plateaus:** athletes new to structured training in a sport improve on almost anything for a few months, then slow (Seiler; research). A stall is no concern until 4 weeks (less trained) to 8 weeks (well trained) of consistent training (Galpin; coach's experience). Before blaming the training for a stall, follow the order in `reviews.md` ("Block review", step 3).
- **Gap analysis:** after each test, express the gap between the goal performance and today as a percentage per sport. Put time where the return is largest, and re-decide after each test, not once a season (Bu; coach's experience).

### When to Retest

- Every 6-8 weeks during base/build phases, or in each recovery week for athletes on a 3:1 or 4:1 pattern
- After recovery weeks (when fresh)
- If perceived effort no longer matches prescribed zones
- After an infection, once resting HR and HRV are back to baseline

---

## Running Pace Zones (VDOT / Jack Daniels)

For athletes with known race times:

| Zone | Name       | Description                  | How to Determine                                  |
| ---- | ---------- | ---------------------------- | ------------------------------------------------- |
| E    | Easy       | Daily running, long runs     | 59-74% VO2max; 1:00-1:30/km slower than threshold |
| M    | Marathon   | Marathon race pace           | 75-84% VO2max; sustainable for 2-4 hours          |
| T    | Threshold  | Tempo runs, cruise intervals | 83-88% VO2max; ~60min race pace                   |
| I    | Interval   | VO2max development           | 95-100% VO2max; 3-5min repeats                    |
| R    | Repetition | Speed, neuromuscular         | > 100% VO2max; short reps with full recovery      |

**Pace Estimation from Threshold:**

- Easy pace: Threshold + 50-70 sec/km
- Marathon pace: Threshold + 15-25 sec/km
- Interval pace: Threshold - 15-20 sec/km
- Repetition pace: Threshold - 25-35 sec/km

---

## Without a Power Meter Outdoors

An athlete with power only on the indoor trainer sets outdoor HR caps from their own indoor rides. Read the HR at the top of their Zone 1 and Zone 2 power on recent steady indoor rides. Those HRs become the outdoor caps, with RPE 4 or less as the easy limit (Claude's judgement). Heat raises HR at the same power, so on hot days outdoors, the HR cap protects the athlete better than any power estimate. Strava's estimated power is not a measurement.

## Power-Based Training (Cycling)

When power data is available, use power zones exclusively—they're more accurate than HR which lags and drifts.

| Workout Type | Zone             | Duration             | Recovery | Weekly Frequency |
| ------------ | ---------------- | -------------------- | -------- | ---------------- |
| Endurance    | 2                | 1-5 hours            | N/A      | 2-4x             |
| Tempo        | 3                | 20-60 min continuous | N/A      | 1-2x             |
| Sweet Spot   | 3-4 (88-93% FTP) | 2x20-30 min          | 5-10 min | 1-2x             |
| Threshold    | 5a               | 2-4 x 8-15 min       | 5-8 min  | 1x               |
| VO2max       | 5b               | 4-6 x 3-5 min        | 3-5 min  | 1x               |
| Anaerobic    | 5c               | 6-10 x 30sec-2min    | 2-4 min  | 0-1x             |
