# V3 Packet Audit - 4 PIQs + 20 Activities + Additional Comments

Audited Nov 26, 2026 (V3). Files: [[piq-required-major]], [[piq-opt-1-leadership]], [[piq-opt-4-barrier]], [[piq-opt-6-community]], [[uc-activities-350char]], [[uc-additional-comments]]. Rules: [[v3-revision-brief]] (overrides earlier notes), [[CLAUDE]], critic rubric from [[committee-review]]. Data: [[courses-and-majors]], [[activities-list]], [[piq-beat-sheets]], [[voice-sample]].

Method: every count and string check below was run by PowerShell script, not by eye. PIQ body = lines after the `Prompt:` line up to the `Word count:` line; words = `($body -split '\s+' | Where-Object { $_ }).Count`. Activity and Box A counts = `.Length` of the text after the colon, compared to the printed `[n/limit]`. The activities file was audited, not regenerated.

## 1. Scorecard (before fix / after fix)

### PIQs

| Check | Required Major | #1 Leadership | #4 Barrier | #6 Community |
|---|---|---|---|---|
| Body 325-350 words (script) | PASS 348 / PASS 348 | PASS 331 / PASS 331 | PASS 349 / PASS 349 | PASS 348 / PASS 348 |
| Printed count matches script | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Plain ASCII, 0 chars > 127 (whole file) | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| No smart quotes, em/en dashes, spaced dashes | PASS 0 / PASS 0 | PASS 0 / PASS 0 | PASS 0 / PASS 0 | PASS 0 / PASS 0 |
| No markdown in body | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Banned words (18) | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Facts to Confirm outside body (after Word count line) | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| No Spring 2027 course claimed as taken | PASS (named only as "This spring I will take") | PASS | PASS | PASS |
| Units phrased "on track" | n/a | n/a | PASS (exact v3 wording) | n/a |
| Study group = Physics 411, Chem 400, CISP 400, ENGR 420 only | n/a | n/a | PASS | n/a |
| Attendance range matches Activity #4 | n/a | n/a | n/a | PASS ("12 to 18" = "12-18") |
| Voice-sample leakage | PASS | PASS (script hit "running the front counter" = false positive) | PASS | PASS |
| Community labeled #6 | n/a | n/a | n/a | PASS (title "Optional PIQ #6") |
| v3 brief goals met | PASS | PASS (outcome first under Facts, labeled) | PASS (MIT OCW cut) | PASS (range, gap closed, active Summit role, library = 1 sentence) |
| MUST-CONFIRM labels consistent across files | PASS | FAIL / PASS | FAIL / PASS | FAIL / PASS |
| EE spine | PASS | n/a | PASS ("every electrical engineering prerequisite") | PASS (hardware builders) |

### Activities ([[uc-activities-350char]]) and Box A ([[uc-additional-comments]])

| Check | Before | After |
|---|---|---|
| 20 entries present, 20 titles and 20 descriptions counted | PASS | PASS |
| Every Title <= 60 chars (range 16-59) | PASS 20/20 | PASS 20/20 |
| Every Org box <= 250 chars (12 boxes, range 107-224) | PASS 12/12 | PASS 12/12 |
| Every Description <= 350 chars (range 188-320) | PASS 20/20 | PASS 20/20 |
| Printed count = actual count (52 fields) | PASS 52/52 | PASS 52/52 |
| Plain ASCII (file) | PASS 0 | PASS 0 |
| No planned course claimed as taken | PASS | PASS |
| Units "on track" (#16) | PASS | PASS |
| Study group courses (#8) | PASS | PASS |
| Attendance #4 = PIQ #6 | PASS | PASS |
| Advisory notes match the v3 PIQs | FAIL (#6 note said the Required PIQ describes Fall work; v3 Required says only "last summer") | PASS |
| Box A Version 1 <= 550 | PASS 534 | PASS 534 |
| Box A Version 2 <= 550 | PASS 507 | PASS 507 |
| Box A plain ASCII, no planned course claimed as taken | PASS | PASS |
| Hours rule (applicant hours kept, Fall total flagged) | PASS | PASS |

Warnings (not failures):
- Activity #10 "Distance Running": the applicant's own 5K/10K training from [[activities-list]], not the voice-sample running-team story. Allowed, already flagged in the activities file. Dropping it is the cleanest way to remove any echo.
- EE spine in Activities: #6 (orbital sim), #15 (MIT OCW aerospace), #18 (orbital debris tool) form an aerospace cluster. Each is real and framed as computation or applied physics, which the brief allows. Do not let #15 be the first Educational Preparation entry a reader sees if order is in your control.

## 2. Overlap table

| PIQ | Story | Evidence used | Opening style | Core trait |
|---|---|---|---|---|
| Required Major | Noise in the signal: telemetry board, then gimbal oscillation, then model vs bench | KiCad/ESP32 board, 50Hz firmware, FLC oscilloscope, STM32 + IMU gimbal, C++ PID, self-taught Laplace/transfer functions/stability margins, 15+ bench tests, RK4 orbital sim (1 sentence), Shashine log habit, Spring 2027 plan | Bench failure in motion ("The code compiled cleanly. The gimbal still would not settle.") | Technical debugging, theory meeting hardware |
| #1 Leadership | Jack in the Box counter vs kitchen blame, fixed through training | Shift Trainer, 4 new hires, POS/food safety, ticket-watching drill, pre-peak staging, callouts, cook agreement, hires running Friday rushes | Line of dialogue ("Where's my food?") | Calm leadership of people under pressure |
| #4 Barrier | Self-built six-college schedule | FLC section limits, Transfer Center ASSIST workshops, spreadsheet, Coastline combined course check, 6 colleges, 4 at once / 8 courses in Summer 2026, Fall courses, study group 6-8 for 3 hrs, 3.97, Honor List, on track for ~74 units | Blunt fact ("three to four years") | Resourcefulness, self-built pathway |
| #6 Community | Empty makerspace to first-time builders at the Tech Summit | Idle makerspace, commuter college, own Tech Summit team (1 paragraph), club workshops biweekly 28 wks in Aspen Hall FL1-130, 12-18 per session, failed first Arduino night, library 10-15 (1 sentence), logistics for 3 teams, demo to judges | Observation of an empty space | Building a builder culture for others |

Result: zero story overlap, zero trait overlap, 4 distinct openings, zero voice-sample leakage.

Evidence lines checked by script across bodies: oscilloscope, gimbal, Shashine (Required only); Jack in the Box (Leadership story, Barrier as a 12 hr/wk constraint only, as allowed); study group, Calc 3, Linear Algebra (Barrier only); makerspace, Aspen Hall, FL1-130, Tech Summit, 12-18 (Community only); MIT OCW (no PIQ). Spring 2027 plan appears only in Required (and Box A, which is Academic History, not a PIQ).

Minor notes:
- Microcontroller work appears in Required (STM32/ESP32) and Community (Arduino nights, own Summit team). Different roles (own build vs teaching others), so not overlap.
- Box A and Barrier both explain the multi-college path. Box A gives the facts; Barrier tells the story. Consistent: six colleges, Spring/Summer 2026, "3-4 years" = "three to four years".
- Closers: Required and Barrier end on concrete facts, Community on a concrete image with a callback ("benches that used to sit empty"), Leadership on its one reflective line. The closer pattern is broken, as the critic asked.

EE spine: Required carries it fully (embedded firmware on STM32/ESP32, KiCad PCB, oscilloscope noise, feedback control, numerical modeling as application) and names circuits, signals and systems, controls, and embedded systems. Barrier frames the plan as "every electrical engineering prerequisite." Community stays on hardware builds. Orbital sim is down to one sentence. PASS.

## 3. Scores (critic rubric, brutal; 8+ stands out in the Berkeley/UCLA EE pool, target 9.0)

### Score table, v1 -> v2 final -> v3

| PIQ | v1 | v2 final | v3 (a) all Facts true | v3 (b) MUST-CONFIRM items false and cut |
|---|---|---|---|---|
| Required Major-Prep | 7.0 | 7.5 | 8.5 | 7.0 |
| #1 Leadership | 7.5 | 8.0 | 8.5 | 6.5 |
| #4 Barrier | 6.0 | 7.0 | 8.5 | 7.5 |
| #6 Community | 6.5 | 7.0 | 8.0 | 6.5 |
| Packet average | 6.75 | 7.375 | 8.375 | 6.875 |

No essay reaches 9.0. Scenario (a) is the ceiling of the current text; scenario (b) is what the packet scores if the invented, load-bearing beats are false and removed without real replacements.

### Sub-scores, scenario (a)

| PIQ | Specificity | Ownership | Prompt coverage | Voice | Tech credibility | Concision | Verdict |
|---|---|---|---|---|---|---|---|
| Required | 9 | 9 | 8 | 8 | 8.5 | 8 | Best technical essay in the packet: the model-vs-bench move is what readers want. Held back by a stock epiphany line and a grab-bag paragraph 4. |
| #1 Leadership | 8.5 | 9 | 9 | 9 | 8 | 8.5 | Strongest voice. The outcome closes the loop but stays modest by design, and the opening scene spends words the dispute could use. |
| #4 Barrier | 8.5 | 9 | 9 | 8.5 | 8 | 8 | Now a real plan with one concrete mapping moment and a concrete ending. The prerequisite logic and the study-group paragraph are the soft spots. |
| #6 Community | 8.5 | 7.5 | 9 | 8 | 8 | 7.5 | Gap opened and closed, with a number and a setback. The applicant's role at the climax is still support work, and two paragraphs sit loose. |

### Sub-scores, scenario (b)

| PIQ | Specificity | Ownership | Prompt coverage | Voice | Tech credibility | Concision | What gets cut |
|---|---|---|---|---|---|---|---|
| Required | 7.5 | 8 | 6.5 | 8 | 7 | 7.5 | Transfer-function model and its prediction, the why-EE oscilloscope moment, the specific diagnosis. Falls back to "self-taught controls + retuned over 15+ tests," and why EE goes missing again. |
| #1 Leadership | 6.5 | 7 | 6 | 8 | 6.5 | 7.5 | Ticket-watching drill, both cook quotes, the call-ahead agreement, the outcome. The "resolve disputes" clause collapses to a paraphrase with no resolution. |
| #4 Barrier | 7 | 8 | 8 | 8 | 7 | 7.5 | Coastline/ASSIST campus-by-campus check and the "math first" prerequisite logic. The barrier and the result survive on real data. |
| #6 Community | 7 | 6 | 7 | 8 | 7.5 | 7.5 | First-time builders demoing at the Summit, the applicant's Summit tasks, all 3 teams building in the makerspace. The ending and the gap-closing callback go with them. |

### Line-level notes behind the scores (no rewrites, levers only)

**Required Major-Prep** ([[piq-required-major]])
1. "That is when I knew I wanted to study electrical engineering." -> stock epiphany phrasing. The moment before it is strong; this sentence announces instead of showing. Cost: Voice.
2. "nothing I changed in the code removed it, because the noise was in the signal itself" -> an EE reader will ask why a digital filter did not help, especially since paragraph 3 fixes the gimbal by filtering in code. Without the hardware change that answered it (filter, grounding, decoupling), the telemetry problem is left unresolved. Cost: Tech credibility. Applicant-only fix.
3. Paragraph 4 ("Last summer I put differential equations... During my Shashine Technologies internship...") -> two unrelated facts in one paragraph. Reads as a checklist. Cost: Concision.
4. "Pitch settled after one small overshoot, close to what the model predicted." -> excellent if true. This is the single line holding the score at 8.5.

**#1 Leadership** ([[piq-opt-1-leadership]])
1. Paragraphs 1-3 (about 70 words) are a freeze scene that does not carry the dispute. Good voice, low prompt load.
2. "running the front counter through Friday rushes without me stepping in" -> observable and modest, as the brief asked. Still not checkable; a reader gives partial credit.
3. "I wanted to cover every station myself. Instead I asked him what was breaking his station." -> the admitted-urge beat works. Keep.
4. 331 words leaves 19 words unused; one real detail only the applicant knows (the real missed modifier) would lift Specificity.

**#4 Barrier** ([[piq-opt-4-barrier]])
1. "Physics 411 and ENGR 420 depend on multivariable calculus and differential equations" -> risky. If the catalog does not list Calc 3 or Diff Eq as prerequisites, the "math first" logic and the closing line both weaken. Cost: Tech credibility.
2. "with classmates carrying loads like mine" -> unsupported generalization. Minor.
3. "The condensed formula sheet I bring each week is also how I study for my own exams." -> flat compared with the rest. The study group still reads a little bolted on.
4. "Before enrolling, I checked ASSIST campus by campus to confirm that one course covered both requirements everywhere I was applying." -> the concrete mapping moment the brief asked for. Strong if true.

**#6 Community** ([[piq-opt-6-community]])
1. Own Tech Summit team paragraph (about 50 words) -> motivation, but it is the applicant's own technical story inside a community essay. Cost: Concision.
2. "Off campus, I assist library staff..." -> one sentence as the brief asked, but it has no link to the makerspace thread. Reads as a resume line.
3. "I booked makerspace bench time... tracked down the parts... set up their tables and power." -> active, but support work. The essay's strongest result ("first-time builders demoed working breadboard prototypes") belongs to the students. Cost: Ownership.
4. "More students stayed until their LED lit." -> vague next to the new 12-18 number.
5. "at the benches that used to sit empty" -> resolves the opening; slightly tidy callback, acceptable.

## 4. Fixes made (V3 audit)

All fixes are outside the essay bodies and outside the activity paste text. No new facts. No essay body, word count, activity paste text, or character count changed.

1. [[uc-activities-350char]], Fall hours table row #6: "required PIQ says work continues this fall" -> "the description applies Physics 411, which is in progress this fall". The v3 Required PIQ no longer says the sim continues in Fall.
2. [[uc-activities-350char]], #6 sanity flag: same stale reference corrected; added the option to label "Summer" and drop the in-progress wording if the work stopped in August.
3. [[piq-required-major]] Facts to Confirm: the diagnosis bullet is now labeled "APPLICANT MUST CONFIRM" (it is load-bearing and interview-testable).
4. [[piq-opt-1-leadership]] Facts to Confirm: three "ESSENTIAL" bullets relabeled "APPLICANT MUST CONFIRM (essential)" so one label means one thing across the packet. The outcome bullet stays first, as the brief requires.
5. [[piq-opt-4-barrier]] Facts to Confirm: the multi-college reason and the mapping moment relabeled "APPLICANT MUST CONFIRM". New MUST CONFIRM bullet for the Physics 411/ENGR 420 prerequisite claim (moved out of the general list and sharpened with a catalog check). The old bullet now covers only the deliberate sequencing.
6. [[piq-opt-6-community]] Facts to Confirm: items 1-3 (attendance range, Summit tasks, first-time builders demo) labeled "APPLICANT MUST CONFIRM".
7. This report overwritten for V3. The old report linked to `piq-opt-7-community`, which no longer exists; all links now point to [[piq-opt-6-community]].

All checks re-run by script after the fixes: 4/4 PIQs 325-350 with matching printed counts (348/331/349/348), 0 non-ASCII characters in all 6 files, 52/52 activity fields and 2/2 Box A versions within limits with matching printed counts.

## 5. Facts to Confirm before submitting (consolidated, all 6 files, prioritized)

### Tier 1 - APPLICANT MUST CONFIRM (load-bearing; if false, cut or replace with what really happened)

1. **Required - model meeting the bench.** You modeled the pitch axis as a transfer function, it showed that heavy IMU filtering would add delay and shrink the stability margin, so you filtered lightly and lowered the derivative gain, and pitch settled after one small overshoot close to the prediction. If you did not model it, cut those sentences and keep noise -> filter -> 15+ bench tests. You must be able to explain this in an interview.
2. **Required - why EE.** The oscilloscope moment on the telemetry board and "nothing I changed in the code removed it, because the noise was in the signal itself." Replace "every sensor reading carried noise" with what the trace actually showed. Be ready for "why didn't a software filter fix it?" If you changed something on the board (filter, grounding, decoupling caps), add it in one clause.
3. **Leadership - outcome (supplied as an example).** New hires "running the front counter through Friday rushes without me stepping in." Swap in your real modest outcome if different. No invented number.
4. **Leadership - the dispute.** The grill cook, "Fix your screen before you send me garbage," weeks of ignored callouts, "Everything hits me at once," the call-ahead agreement, and that he stopped yelling. If no real quotes, paraphrase without quotation marks.
5. **Leadership - the training drill.** New hires ringing practice orders and watching their tickets come up on the line. "No cheese" is a placeholder; use the modifier that really kept getting missed.
6. **Community and Activity #4 - attendance.** "12 to 18 students" (PIQ #6) and "12-18 students per session" (Activity #4) is an applicant-supplied range. Replace with your real typical number in both places, identically.
7. **Community - the result and your role.** Some Summit team members wired their first circuit at a club Arduino night; they demoed working breadboard prototypes to faculty judges; all three teams built in the makerspace; you booked bench time, tracked down parts, and set up tables and power. Cut any part that did not happen.
8. **Barrier - mapping moment and prerequisite logic.** FLC's Calc 3 and Diff Eq/Linear Algebra sections would not fit one summer; you checked ASSIST campus by campus that Coastline's combined course covered both requirements; Physics 411 and ENGR 420 "depend on" Calc 3 and Diff Eq (check the Los Rios catalog). Also confirm the articulation itself on ASSIST.
9. **Required - diagnosis.** The derivative term reacting to IMU noise and kicking the motors, fixed by light filtering plus a lower derivative gain. Word for word.
10. **Barrier - multi-college reason.** Every outside college was "for a seat or time slot FLC could not give me," including Foothill and Palomar in Spring 2026. If cost or online format also applied, add it in your own words (and in Box A).
11. **Box A - CVC.** Use Version 1 only if you really enrolled through the California Virtual Campus Exchange. Otherwise use Version 2.

### Tier 2 - Confirm (specific claims a reader could check)

12. Activity #18: Honorable Mention vs participation only. If participation, retitle and move to Extracurricular.
13. Activity #8: 28 wks/yr for a study group whose courses are Fall 2026 only. Use your real weeks.
14. Activity #16 and Barrier: President's and Dean's Honor List "every semester"; name only the terms you actually received it (no summer terms; Spring/Summer 2026 units were mostly at other colleges).
15. Barrier: "six colleges" and "four of them at once" (if CISP 360 was at a Los Rios college other than FLC, the total may be seven; fix Barrier and Box A together).
16. Barrier and Box A: the "three to four years" estimate, and "if I missed one seat, every course behind it would slip a full year" (cut if not true).
17. Required and Box A: Physics 411/421/431 is the full calculus-based physics sequence for your campuses (ASSIST).
18. Community and Activity #4: you led the sessions yourself ("ran" in the PIQ, "Plan and lead" in the activity; the source says "coordinated"). Activity #4 also says "Organized club study nights" and "Ran logistics"; the source says "Helped organize" and "assisted with logistics." Use the verb that is true.
19. Activity #3: students "raised their test averages by a full letter grade."
20. Activity #9: wiring was your part of the team build ("Handled the sensing and actuation wiring"). Activity #9 vs #19: same prototype ("small-scale solar-tracking panel" vs "dual-axis solar-tracking prototype").
21. Activity #5 and Required: the STM32 drives both pitch and yaw.
22. Activity hours: the Fall total reads 35-42 hrs/wk beside an 18-unit load and the 12 hr/wk job. Label the real terms for #6, #13, #14, #20 (and #11 if mostly summer/holidays). Do not change your numbers, only the labels.
23. Box A: if CISP 360 or Spring 2027 courses are at a Los Rios college other than FLC, name it.

### Tier 3 - Scene and detail checks (low risk, but must be true)

24. Required: build order (telemetry board before gimbal), clean-compile and nudging opening, "changing one value at a time," "beyond what my FLC courses covered," orbital sim built during or after Summer 2026 Diff Eq, the Shashine test-log habit (fallback wording is in the file).
25. Leadership: "Where's my food?", the hire freezing at the register you trained her on, "Combo first, then the drink," hearing your hires blame the kitchen, pre-peak staging, "Big order coming," "within a few months."
26. Barrier: Transfer Center workshops as where you learned ASSIST, the spreadsheet, "four course portals open and a shift the next day," the doubt about grades, study group details (six to eight, three hours weekly, whiteboards, formula sheet).
27. Community: makerspace nearly empty most afternoons, "few knew the makerspace was open to them," your own Summit team timeline and "for hours," the 3 rotated topics, the failed first Arduino night and the one-circuit fix, library role (debugging Scratch and Python).
28. Activity #7: "Laid out" vs "Designed and assembled" (if the PCB was fabricated). Activity #17: pick "School" unless AMATYC ranked you nationally. Activity #20: move to Extracurricular if the Other Coursework box asks for a course number. Activity #10: keep or drop.
29. Grades: report Fall 2026 grades on the Transfer Academic Update by Jan 31, 2027.
30. Prompt number: paste the community essay into Optional #6.

**Integrity:** UC requires you to certify the PIQs are your own work. Read every final aloud and rewrite any line that does not sound like you before submitting.
