# Required Major-Prep PIQ - v3
Prompt: Please describe how you have prepared for your intended major, including your readiness to succeed in your upper-division courses once you enroll at the university.

The code compiled cleanly. The gimbal still would not settle. My STM32 read the IMU and drove both axes of my thrust-vectoring test stand. When I nudged the mount, pitch swung past level, came back, and swung harder.

I had seen this before. Months earlier, I laid out a telemetry board in KiCad with an ESP32, a barometric altimeter, and an SD logger. I soldered its through-hole and surface-mount parts and wrote C++ firmware that samples at 50Hz. On an FLC lab oscilloscope, the sensor signal showed noise on every reading, and no change to my code could remove it. The problem was in the signal itself. That is when I knew I wanted to study electrical engineering.

The gimbal had the same problem. My C++ PID loop had a derivative term that reacted to each spike of IMU noise and kicked the motors. To understand why that made it oscillate, I taught myself Laplace transforms, transfer functions, and stability margins, beyond FLC's courses. Then I modeled the pitch axis as a transfer function. The model showed that a heavy filter on the IMU would add delay and shrink my stability margin, so I filtered lightly and lowered the derivative gain. Across 15+ bench tests, I changed one value at a time and logged the response. Pitch settled after one small overshoot, close to what the model predicted.

Last summer's differential equations course also let me build an orbital simulator in Python and C++ with 4th-order Runge-Kutta. As a Shashine Technologies intern, I automated data validation in Python and learned to bring senior engineers the test log that reproduced a bug before asking for help.

Upper-division EE will give formal tools to problems I have already hit on my bench. The noise on my board is signals and systems. Tuning the gimbal against a model is controls. The STM32 and ESP32 firmware is embedded systems, and the board itself is circuits. This spring I will take Physics 421, Physics 431, and ENGR 400, finishing the calculus-based physics sequence before I enroll.

Word count: 341

Facts to Confirm:
- APPLICANT MUST CONFIRM - model meeting the bench (added in v3 to answer the critic's top point): "I modeled the pitch axis as a transfer function. The model showed that a heavy filter on the IMU would add delay and shrink my stability margin, so I filtered lightly and lowered the derivative gain... Pitch settled after one small overshoot, close to what the model predicted." None of this is in your data beyond Activity #20 (self-studied Laplace, transfer functions, stability margins). If you did not actually model the loop, cut those sentences and keep only: noise -> filtered the IMU -> retuned across 15+ bench tests. Never ship a model you cannot explain in an interview.
- APPLICANT MUST CONFIRM - why EE: "the sensor signal showed noise on every reading, and no change to my code could remove it. The problem was in the signal itself. That is when I knew I wanted to study electrical engineering." Built from Activity #7 (oscilloscope noise testing). Confirm this is your real reason. If you changed something on the board because of the trace (a filter, grounding, decoupling caps), add it in one clause: it would make this stronger. "Noise on every reading" is a writer's guess at what the trace showed; replace it with what you saw.
- Diagnosis: the derivative term reacting to IMU noise and kicking the motors, fixed by light filtering plus a lower derivative gain. Confirm the real cause and fix word for word.
- Build order: "Months earlier" assumes the telemetry board (Spring/Summer) came before the gimbal (Summer/Fall). Fix if wrong.
- Opening scene (clean compile, nudging the mount, pitch swinging harder) and the tuning method ("changed one value at a time and logged the response").
- "Beyond FLC's courses": assumes no FLC course you took taught Laplace transforms, transfer functions, or stability margins.
- Orbital sim: "Last summer's differential equations course also let me build" assumes the sim was built during or after Summer 2026. The FEA bracket clause and the Physics 411 sim detail from the final were cut to keep the essay on EE.
- Shashine: "learned to bring senior engineers the test log that reproduced a bug before asking for help." Fallback if not true: "troubleshot edge-case bugs with senior engineers and organized testing logs for internal tooling."
- "Finishing the calculus-based physics sequence": confirm on ASSIST that Physics 411/421/431 is the full sequence for your campuses. Physics 421, 431, and ENGR 400 are Spring 2027 plans only. Optional: you may add "with Prof. Dan Ross" after ENGR 400 (instructor of an upcoming course only; claim no past contact).
- No faculty work is claimed, since none exists in the data. Fall courses (CISP 400, ENGR 420) were cut as a transcript list; the application already shows them.
- Read the final aloud and rewrite any line that does not sound like you. UC requires you to certify the PIQs are your own work.

Sub-clauses answered:
- (a) How interest in EE developed -> paragraph 2: oscilloscope noise on the self-designed telemetry board that code could not fix.
- (b) Preparation in and out of class -> paragraphs 2-4: KiCad/ESP32 board and 50Hz firmware, gimbal PID diagnosis, self-studied controls with a transfer-function model checked on the bench across 15+ tests, Summer 2026 differential equations and the RK4 sim (one sentence), Shashine internship. No faculty work claimed.
- (c) Readiness for upper-division courses -> paragraph 5: maps the bench work to signals and systems, controls, embedded systems, and circuits, then names Spring 2027 Physics 421, Physics 431, and ENGR 400 as planned only.
