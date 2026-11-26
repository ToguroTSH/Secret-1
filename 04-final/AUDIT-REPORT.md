# Final Packet Audit - 4 PIQs + 20 Activities

Audited Nov 26, 2026. Files: [[piq-required-major]], [[piq-opt-1-leadership]], [[piq-opt-4-barrier]], [[piq-opt-7-community]], [[uc-activities-350char]]. Checked against [[courses-and-majors]], [[activities-list]], [[piq-beat-sheets]], [[voice-sample]], [[winning-patterns]].

Word counts, ASCII, markdown, dashes, banned words, voice-sample leakage, and planned-course mentions were all checked by PowerShell script, not by eye. Body = text between the Prompt line and the "Word count:" line; words = `($body -split '\s+' | Where-Object { $_ }).Count`.

## IMPORTANT: prompt number for the community essay
The community prompt ("What have you done to make your school or your community a better place?") is likely **#6** on the live UC transfer application. The vault calls it #7, which is the freshman number; on the transfer page #7 is the "strong candidate" prompt. Confirm the number in the application portal before pasting [[piq-opt-7-community]]. The essay answers the community prompt either way, so no text changes are needed, only the right box.

## 1. Scorecard (before fix / after fix)

| Check | Required Major | #1 Leadership | #4 Barrier | Community (#6 or #7) |
|---|---|---|---|---|
| Word count 325-350 | PASS 345 / PASS 349 | PASS 347 / PASS 347 | PASS 339 / PASS 339 | PASS 335 / PASS 335 |
| Declared count matches script | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Plain ASCII (no char > 127) | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| No markdown in body | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Dashes (0-1 hyphen-dash, no em/en) | PASS 0 / PASS 0 | PASS 0 / PASS 0 | PASS 0 / PASS 0 | PASS 0 / PASS 0 |
| Banned words (18) | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Voice-sample leakage | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Planned courses only as upcoming | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Numbers traceable to 00-context | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Facts consistent with Activities list | FAIL / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Prompt alignment | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| Distinct opening style | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |
| AI cadence (no not-X-but-Y, triads, tidy closers) | PASS / PASS | PASS / PASS | PASS / PASS | PASS / PASS |

Activities ([[uc-activities-350char]]): 20/20 entries at or under 350 characters (range 179-291), 0 non-ASCII characters in the file, all 3 consistency flags from [[activities-list]] fixed. PASS.

Only failure: Required PIQ said "Next I laid out a telemetry board", which put the telemetry board after the gimbal. The Activities list dates the board Spring/Summer and the gimbal Summer/Fall, so a reader comparing the two would see the order reversed. Fixed (see section 5).

## 2. Cross-PIQ overlap table

| PIQ | Story | Evidence used | Opening style | Core trait |
|---|---|---|---|---|
| Required Major | Gimbal oscillation to telemetry noise to readiness | Gimbal/STM32/PID/15+ tests, Fusion 360 FEA, self-study controls, KiCad/ESP32 board at 50Hz, RK4 orbital sim, Shashine QA | Bench failure in motion ("The code compiled cleanly.") | Technical debugging, theory to hardware |
| #1 Leadership | Jack in the Box rush and counter-kitchen conflict | Shift Trainer, 4 new hires, POS/food safety, callouts, pre-peak staging, cook agreement | Line of dialogue ("Where's my food?") | Calm leadership of people under pressure |
| #4 Barrier | Self-built multi-college schedule | ASSIST mapping, Transfer Center workshops, 6 colleges, 8 courses at 4 colleges in Summer 2026, MIT OCW, study group 6-8, 74 units, 3.97, Honor List | Blunt fact ("three to four years") | Resourcefulness, self-built pathway |
| Community | Hands-on builder culture at a commuter college | Idle Innovation Center, own Tech Summit team, club workshops (28 wks, FL1-130, 3 topics), library 10-15, FRC/VEX 8-week season, 3 Summit teams | Observation of an idle space | Building a builder culture for others |

Result: zero story overlap, zero trait overlap, 4 distinct openings, zero leakage of meditation, BrighterMinds, Arjun, running/cross-country, Nikhil, Coach Esayas, box-breathing, or panic attacks.

Minor notes (not failures):
- Course names repeat: Required and Barrier both name Calc 3, Diff Eq/Linear Algebra, Physics 411, and ENGR 420. Barrier uses them for sequencing, Required for readiness. This is shared transcript context, not shared story evidence.
- Jack in the Box shows up in Barrier only as a constraint ("12 hours a week"), as the beat sheet allows.
- The 3D-printed mounts (Required) were made at the Innovation Center (Community setting), but Required does not name the Center, so there is no visible overlap.

## 3. Prompt alignment

**Required Major-Prep**
- How you prepared for the major, interest: answered. "Tracing that noise on a board I had designed is when I knew I wanted to study sensing and firmware."
- Preparation in and out of class: answered. "Last summer, after Calc 3 and Differential Equations with Linear Algebra, I built an orbital simulator..." / "At Shashine Technologies, I wrote Python scripts..."
- Readiness for upper-division courses: answered. "Upper-division controls means building a model on paper and making hardware match it. I did that for the first time on the gimbal."

**#1 Leadership**
- Leadership experience: answered. "As Shift Trainer for 4 new hires, I started hearing them blame the kitchen too, so I changed how I trained them."
- Positively influenced others: answered. "Over the following months, the new hires made callouts without prompting."
- Helped resolve disputes: answered. "We agreed the counter would call large orders before ringing them in."
- Contributed to group efforts over time: answered. "For weeks, one cook ignored the callouts..." plus "Over the following months..."

**#4 Barrier**
- Educational barrier named: answered. "At Folsom Lake College's pace, my engineering prerequisites would have taken three to four years."
- How you worked to overcome it: answered. "So I built the schedule myself." / "That plan took me to six colleges."
- Taken advantage of an opportunity (supporting): answered. "Over breaks I worked through MIT OpenCourseWare modules..."
- Result: answered. "My grades held." / "This fall I started Physics 411 and ENGR 420 with the math already finished."

**Community**
- What you have done: answered. "As Workshops Coordinator for the FLC Math & Engineering Club, I organized hands-on sessions every other week across 28 weeks..."
- School or community: answered. Both school (club, Tech Summit) and community ("Off campus, I assist library staff...").
- Made it better (result): answered. "More of them stayed until their LED lit." / "I watched them demo working breadboard prototypes to faculty judges."

## 4. Strict compliance detail
- Planned Spring 2027 courses appear only in Required, only as "This spring I will take Physics 421, Physics 431, and ENGR 400". No other PIQ names them.
- Numbers found and traced: Required (STM32, 15+, ESP32, 50Hz, 2-body, 4th-order, CISP 360/400, Physics 411, ENGR 420) to Activities #5-7 and the course table; Leadership (4) to Activity #2; Barrier (12 hrs, Summer 2026, 4 colleges, 8 courses, 6 colleges, 3 hrs, 6-8, 74 units, 3.97) to Activities #2, #8, #16 and the course table; Community (28 weeks, FL1-130, 3 topics, 10-15, 8-week, 3 teams, team of 4) to Activities #4, #9, #12, #13.
- Hyphens in all 4 bodies are compound words or ranges (3D-printed, edge-case, 10-15, FL1-130), not dashes.

## 5. Fixes made
1. [[piq-required-major]], paragraph 3: "Next I laid out a telemetry board" changed to "Earlier, I had laid out a telemetry board"; "the data showed the same noise that had thrown off the gimbal" changed to "its data showed the same kind of sensor noise that later threw off the gimbal". This makes the order match the Activities dates. No new facts. Word count 345 to 349 (re-checked by script). The "Facts to verify" bullet was updated to match, and a timing bullet for the orbital sim was added.
2. [[uc-activities-350char]] created: 20 entries, each with category, title, hours/weeks, description, and a script-counted character total. Consistency fixes: #4 Physics 421 removed, #8 Physics 431 removed, #16 Engineering no longer claimed as completed, #6 Physics 411 marked in progress, #14 "UC Davis" generalized to "university".
3. No changes to [[piq-opt-1-leadership]], [[piq-opt-4-barrier]], or [[piq-opt-7-community]]. Every check passed.

## 6. Facts to verify with applicant (all 4 PIQs + activities)

**Required Major** ([[piq-required-major]])
- WHY EE line ("Tracing that noise... sensing and firmware") was written for you. Confirm it, or replace it with your real reason.
- Build order: the telemetry board came before the gimbal (changed in audit to match the Activities dates). Revert to "Next I laid out" if the gimbal came first.
- The oscilloscope showed noise on the telemetry data.
- The diagnosis: the derivative term reacting to IMU noise, fixed by filtering. You must be able to explain this in an interview, or cut it.
- Opening scene (clean compile, nudging the mount, swinging harder), and "changed one value at a time".
- Fusion 360 stress plots were used on the gimbal brackets specifically.
- "Beyond FLC's courses" for Laplace transforms, transfer functions, and stability margins.
- The orbital sim was built "after" Calc 3 and Diff Eq/LA (all were Summer 2026), and Physics 411 work on it is ongoing this fall.
- Standup lesson about bringing the test log.
- Physics 411/421/431 complete the calc-based physics sequence for your campuses (check ASSIST).

**#1 Leadership** ([[piq-opt-1-leadership]])
- "Where's my food?", the Friday-rush details, the new hire who froze, and "Combo first, then the drink."
- The cook's quote "Fix your screen before you send me garbage." Paraphrase it if nobody really said it.
- Your new hires starting to blame the kitchen as the reason you changed training.
- ESSENTIAL: practice orders watched on the kitchen line.
- Pre-peak staging and the "Big order coming" callout.
- ESSENTIAL: the cook who ignored callouts for weeks, "Everything hits me at once," the agreement, and the result.
- "Over the following months" and new hires making callouts unprompted.

**#4 Barrier** ([[piq-opt-4-barrier]])
- Limited sections, waitlisted labs, time conflicts, and the "three to four years" estimate.
- "Every course behind it would slip a full year."
- Transfer Center workshops as where you learned ASSIST, then mapped it yourself.
- The spreadsheet logged before registering.
- The reason for using several colleges (access and schedule only, or also cost).
- "Four of them at once" in Summer 2026 (Coastline, Sierra, Long Beach City, Los Rios).
- "Four course portals open and a shift the next day," and the doubt about grades.
- MIT OCW problem sets done, and aerodynamics/propulsion as the topics you wanted next.
- Study group origin, and that the Calc 3/Diff Eq sequencing was deliberate.
- NEW (audit): "I have about 74 units". Your course file says the ~74 units is the total transfer sequence, and the Honor List entry says 70+. Confirm 74 is what you have now, or change it to "I am on track for about 74 units".
- Honor List every semester, including terms with most units from other colleges.

**Community** ([[piq-opt-7-community]])
- Idle Innovation Center printers "most afternoons," and "nobody had told them" it was open.
- Your Tech Summit team as the motivation, the timeline, "for hours" on the power-draw problem, and whether your team was one of the 3.
- Python sessions meant to replace plotting by hand.
- The failed first Arduino night, cutting to one circuit, pointing to the breadboard section, and "more of them stayed."
- Summit team members first touching a microcontroller at your workshops, and the breadboard demos to judges.
- PROMPT NUMBER: likely #6 on the live transfer application. Confirm in the portal.

**Activities** ([[uc-activities-350char]])
- #3: the full-letter-grade improvement.
- #10: distance running (your own 5K/10K training, no team) kept as listed. Keep or drop it.
- #16: 70+ vs about 74 units, and every semester.
- #18: Honorable Mention vs participant.
- #9 vs #19: small-scale vs dual-axis description of the same prototype.

**Integrity:** UC requires you to certify the PIQs are your own work. Read every final aloud and rewrite any line that does not sound like you before submitting.
