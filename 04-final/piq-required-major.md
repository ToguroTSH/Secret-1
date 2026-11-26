# Required Major-Prep PIQ - FINAL
Prompt: Please describe how you have prepared for your intended major, including your readiness to succeed in your upper-division courses once you enroll at the university.

The code compiled cleanly. The gimbal still would not settle. My STM32 read the IMU and drove both axes of my thrust-vectoring test stand. When I nudged the mount, pitch swung past level, came back, and swung harder.

I designed the stand in Fusion 360 and used stress plots to reinforce its 3D-printed brackets. To hold it steady, I wrote a PID loop in C++. My first gains were guesses. Across 15+ bench tests, I changed one value at a time and logged the response. The swing came from the derivative term reacting to sensor noise, so I filtered the IMU signal before tuning again. To understand why it oscillated, I taught myself Laplace transforms, transfer functions, and stability margins, beyond FLC's courses.

Earlier, I had laid out a telemetry board in KiCad with an ESP32, a barometric altimeter, and an SD logger. I soldered through-hole and surface-mount parts and wrote C++ firmware that samples at 50Hz. On an FLC lab oscilloscope, its data showed the same kind of sensor noise that later threw off the gimbal. Tracing that noise on a board I had designed is when I knew I wanted to study sensing and firmware.

Last summer, after Calc 3 and Differential Equations with Linear Algebra, I built an orbital simulator in Python and C++ that models 2-body transfers and atmospheric drag with 4th-order Runge-Kutta. This fall I am adding Physics 411 dynamics to it, and I check its results against published textbook benchmarks.

At Shashine Technologies, I wrote Python scripts that automated data validation and ran QA test cases. In weekly standups, I troubleshot edge-case bugs with senior engineers. I learned to bring the test log that reproduced a bug before asking for help.

Upper-division controls means building a model on paper and making hardware match it. I did that for the first time on the gimbal. I finished CISP 360 last summer, and this fall I am taking Physics 411, CISP 400, and ENGR 420. This spring I will take Physics 421, Physics 431, and ENGR 400, completing the calculus-based physics sequence before I enroll.

Word count: 349
Facts to verify with applicant:
- WHY EE (written for you, not taken from your answers): "Tracing that noise on a board I had designed is when I knew I wanted to study sensing and firmware." It comes from Activity #7 (oscilloscope noise testing). Confirm it is true, or replace it with your real reason in one sentence.
- Build order (changed in audit): the essay now says "Earlier, I had laid out a telemetry board" and "the same kind of sensor noise that later threw off the gimbal", to match the Activities list (telemetry board Spring/Summer, gimbal Summer/Fall). Confirm the board came first and that the oscilloscope showed noise on its data. If the gimbal actually came first, change "Earlier, I had laid out" back to "Next I laid out".
- "Last summer, after Calc 3 and Differential Equations with Linear Algebra, I built an orbital simulator": both math courses were Summer 2026 too. Confirm the sim was built after them (or during them).
- Diagnosis (must be exact): the derivative term reacting to IMU noise, fixed by filtering the IMU signal before retuning. If this is not what happened, give the real cause and fix. If you cannot explain it in an interview, cut it and keep only the 15+ bench tests.
- Opening scene: clean compile, nudging the mount, pitch overshooting and swinging harder.
- Tuning method: "changed one value at a time and logged the response."
- FEA clause: that the Fusion 360 stress plots (Activity #20) were used on the gimbal's brackets specifically.
- Self-study: "beyond FLC's courses" assumes FLC does not teach Laplace transforms, transfer functions, or stability margins in the courses you took. Confirm.
- "This fall I am adding Physics 411 dynamics to it": Activity #6 says the sim applies Physics 411. Confirm the work is ongoing this fall.
- Standup lesson: "I learned to bring the test log that reproduced a bug before asking for help." Fallback if not true: "I troubleshot edge-case bugs with senior engineers and organized testing logs for internal tooling."
- "Completing the calculus-based physics sequence": assumes Physics 411, 421, and 431 make up the full sequence for your target campuses. Confirm on ASSIST.
- Physics 421, Physics 431, and ENGR 400 are Spring 2027 plans only. Do not let any edit make them sound completed.
- Read the final aloud and rewrite any line that does not sound like you before submitting. UC requires you to certify the PIQs are your own work.
