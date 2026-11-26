# Required Major-Prep PIQ - v2
Prompt: Please describe how you have prepared for your intended major, including your readiness to succeed in your upper-division courses once you enroll at the university.

The code compiled cleanly. The gimbal still would not settle. My STM32 read the IMU and drove both axes of my thrust-vectoring test stand. When I nudged the mount, pitch swung past level, came back, and swung harder.

I designed the stand in Fusion 360 and used stress plots to reinforce its 3D-printed brackets. To hold it steady, I wrote a PID loop in C++. My first gains were guesses. Across 15+ bench tests, I changed one value at a time and logged the response. The swing came from the derivative term reacting to sensor noise, so I filtered the IMU signal before tuning again. To understand the oscillation, I taught myself Laplace transforms, transfer functions, and stability margins, beyond FLC's curriculum.

Noise followed me to my next build. I laid out a telemetry board in KiCad with an ESP32, a barometric altimeter, and an SD logger. I soldered through-hole and surface-mount parts and wrote C++ firmware that samples at 50Hz. On an FLC lab oscilloscope, I saw the gimbal's problem again: noise on the data. Tracing noise on a board I designed is when I knew sensing and firmware were what I wanted to study.

Last summer, after Calc 3 and Differential Equations with Linear Algebra, I built an orbital simulator in Python and C++ that models 2-body transfers and atmospheric drag with 4th-order Runge-Kutta. This fall I am adding Physics 411 dynamics to it, and I verify its results against published textbook benchmarks.

At Shashine Technologies, I wrote Python scripts that automated data validation and ran QA test cases. In weekly standups, I troubleshot edge-case bugs with senior engineers and learned to bring the test log that reproduced a bug before asking for help.

Upper-division controls asks for a model on paper that hardware matches on the bench. The gimbal is where I first did both. I finished CISP 360 last summer, and this fall I am taking Physics 411, CISP 400, and ENGR 420. This spring I will take Physics 421, Physics 431, and ENGR 400, completing the calculus-based physics sequence before I enroll.

Word count: 347

Sub-clauses answered:
- (a) How interest in EE developed -> paragraph 3, last sentence: tracing noise on the telemetry board's oscilloscope trace pulled the applicant toward sensing and firmware (built from Activity #7; applicant must confirm, see below).
- (b) Preparation in and out of class -> paragraphs 1-5: gimbal PID tuning over 15+ bench tests, Fusion 360 FEA on brackets, self-studied controls (Activity #20), KiCad/ESP32 telemetry board with 50Hz firmware and oscilloscope noise testing, RK4 orbital simulator built on Calc 3, Diff Eq/Linear Algebra, and Physics 411, Shashine internship. No faculty work exists in the data, so none is claimed.
- (c) Readiness for upper-division courses -> final paragraph: ties upper-division controls to the gimbal model-vs-bench work, names completed (Calc 3, Diff Eq/LA in paragraph 4; CISP 360) and in-progress courses (Physics 411, CISP 400, ENGR 420), names Spring 2027 Physics 421, Physics 431, and ENGR 400 as planned only.

Facts to verify with applicant:
- WHY EE (built by the writer, not from you): "Tracing noise on a board I designed is when I knew sensing and firmware were what I wanted to study." It is built from Activity #7 (oscilloscope noise testing). Confirm it is true, or replace it with your real reason in one sentence.
- "Noise followed me to my next build" and "saw the gimbal's problem again": assumes the telemetry board came after the gimbal and that the oscilloscope showed noise on the data. Activity #7 is Spring/Summer and the gimbal is Summer/Fall, so the order may be wrong. If the board came first, reorder or say "The same problem showed up on my telemetry board."
- Diagnosis (essential, must be exact): the derivative term reacting to IMU noise, fixed by filtering the IMU signal before retuning. If this is not what happened, give the real cause and fix. If you cannot explain it in an interview, it comes out and the paragraph keeps only the 15+ bench tests.
- Opening scene: clean compile, nudging the mount, pitch overshooting and swinging harder.
- "Changed one value at a time and logged the response" as your tuning method.
- FEA clause: that the Fusion 360 stress plots (Activity #20) were used on the gimbal's brackets specifically.
- "This fall I am adding Physics 411 dynamics to it": Activity #6 says the sim applies Physics 411. Confirm the work is ongoing this fall.
- Standup lesson: "learned to bring the test log that reproduced a bug before asking for help." Fallback if not true: "troubleshot edge-case bugs with senior engineers and organized testing logs for internal tooling."
- "Completing the calculus-based physics sequence": assumes Physics 411, 421, 431 is the full sequence for your target campuses. Confirm on ASSIST.
- Read the final aloud and rewrite any line that does not sound like you before submitting.
