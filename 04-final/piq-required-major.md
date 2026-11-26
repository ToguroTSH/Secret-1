# Required Major-Prep PIQ - FINAL
Prompt: Please describe how you have prepared for your intended major, including your readiness to succeed in your upper-division courses once you enroll at the university.

The code compiled cleanly. The gimbal still would not settle. My STM32 read the IMU and drove both axes of my thrust-vectoring test stand. When I nudged the mount, pitch swung past level, came back, and swung harder.

Months earlier, I had laid out a telemetry board in KiCad with an ESP32, a barometric altimeter, and an SD logger. I soldered its through-hole and surface-mount parts and wrote C++ firmware that samples at 50Hz. On an FLC lab oscilloscope, every sensor reading carried noise, and nothing I changed in the code removed it, because the noise was in the signal itself. That is when I knew I wanted to study electrical engineering.

The gimbal had the same problem. The derivative term in my C++ PID loop reacted to every spike of IMU noise and kicked the motors. To understand why that made it oscillate, I taught myself Laplace transforms, transfer functions, and stability margins, beyond what my FLC courses covered. Then I modeled the pitch axis as a transfer function. It showed that heavy filtering on the IMU would add delay and shrink my stability margin, so I filtered lightly and lowered the derivative gain instead. I ran 15+ bench tests, changing one value at a time and logging the response. Pitch settled after one small overshoot, close to what the model predicted.

Last summer I put differential equations to work in an orbital simulator I wrote in Python and C++ with 4th-order Runge-Kutta. During my Shashine Technologies internship, I automated data validation in Python. I also learned to bring senior engineers the test log that reproduced a bug before I asked for help.

Upper-division EE will give me formal tools for problems I have already hit on my bench. The noise on my telemetry board is a signals and systems problem. Controls is the theory behind tuning the gimbal against its model, and embedded systems and circuits cover the STM32 and ESP32 firmware and the board itself. This spring I will take Physics 421, Physics 431, and ENGR 400, finishing the calculus-based physics sequence before I enroll.

Word count: 348

Facts to Confirm:
- APPLICANT MUST CONFIRM - model meeting the bench: "Then I modeled the pitch axis as a transfer function. It showed that heavy filtering on the IMU would add delay and shrink my stability margin, so I filtered lightly and lowered the derivative gain instead... Pitch settled after one small overshoot, close to what the model predicted." Nothing in your data supports this beyond Activity #20 (self-studied Laplace, transfer functions, stability margins). If you did not actually model the loop, cut those sentences and keep only: noise -> filtered the IMU -> retuned across 15+ bench tests. Never ship a model you cannot explain in an interview.
- APPLICANT MUST CONFIRM - why EE: "every sensor reading carried noise, and nothing I changed in the code removed it, because the noise was in the signal itself. That is when I knew I wanted to study electrical engineering." Built from Activity #7 (oscilloscope noise testing). Confirm this is your real reason. If you changed something on the board because of the trace (a filter, grounding, decoupling caps), add it in one clause. "Every sensor reading carried noise" is a writer's guess at what the trace showed; replace it with what you saw.
- APPLICANT MUST CONFIRM - diagnosis: the derivative term reacting to IMU noise and kicking the motors, fixed by light filtering plus a lower derivative gain. Confirm the real cause and fix word for word.
- Build order: "Months earlier" assumes the telemetry board (Spring/Summer) came before the gimbal (Summer/Fall). Fix if wrong.
- Opening scene (clean compile, nudging the mount, pitch swinging harder) and the tuning method ("changing one value at a time and logging the response").
- "Beyond what my FLC courses covered": assumes no FLC course you took taught Laplace transforms, transfer functions, or stability margins.
- Orbital sim: "Last summer I put differential equations to work in an orbital simulator" assumes the sim was built during or after your Summer 2026 Differential Equations with Linear Algebra course.
- Shashine: "learned to bring senior engineers the test log that reproduced a bug before I asked for help." Fallback if not true: "troubleshot edge-case bugs with senior engineers and organized testing logs for internal tooling."
- "Finishing the calculus-based physics sequence": confirm on ASSIST that Physics 411/421/431 is the full sequence for your campuses. Physics 421, 431, and ENGR 400 are Spring 2027 plans only. Optional: you may add "with Prof. Dan Ross" after ENGR 400 (instructor of an upcoming course only; claim no past contact).
- No faculty work is claimed, since none exists in the data. Fall courses (CISP 400, ENGR 420) are left to the transcript.
- Read the final aloud and rewrite any line that does not sound like you. UC requires you to certify the PIQs are your own work.
