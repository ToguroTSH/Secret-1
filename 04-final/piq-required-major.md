# Required Major-Prep PIQ - FINAL
Prompt: Please describe how you have prepared for your intended major, including your readiness to succeed in your upper-division courses once you enroll at the university.

The code compiled cleanly. The gimbal still would not settle. My STM32 read the IMU and drove both axes of my thrust-vectoring test stand. When I nudged the mount, pitch swung past level, came back, and swung harder.

Months earlier, I had laid out a telemetry board in KiCad with an ESP32, an altimeter, and an SD logger. On an FLC lab oscilloscope, the 3.3V rail spiked 200 to 300 mV whenever the ESP32 wrote to the SD card. A moving-average filter in my firmware only added lag to my 50Hz readings and could not stop spikes corrupting each read. So I fixed the board. I soldered a 0.1 uF decoupling capacitor at the altimeter's power pins and a 10 uF bulk capacitor at the SD module, and rerouted the ground so SD writes stopped sharing the sensor's return path. The trace went flat. That was when I knew I wanted to study circuits and power delivery and fix problems at the source.

The gimbal had its own noise problem. The derivative term in my C++ PID loop reacted to every spike of IMU noise and kicked the motors. To see why, I taught myself Laplace transforms, transfer functions, and stability margins, beyond what my FLC courses covered. Then I modeled the pitch axis as a transfer function. It showed that heavy filtering would add delay and shrink my stability margin, so I filtered lightly and lowered the derivative gain. Over 15+ bench tests, changing one value at a time, pitch settled after one small overshoot, close to what the model predicted.

Last summer I also wrote a Runge-Kutta orbital simulator in Python and C++. As a Shashine Technologies intern, I automated data validation in Python and learned to bring engineers the test log that reproduced a bug.

Upper-division EE will formalize problems I have already hit on my bench: signals and systems for the noise, controls for the gimbal, circuits and embedded systems for the boards and firmware. This spring I will take Physics 421, Physics 431, and ENGR 400, finishing the calculus-based physics sequence before I enroll.

Word count: 349

Facts (applicant-confirmed):
Applicant confirmed all items below as true on Nov 26, 2026. Kept for reference (interview prep).
- CONFIRMED by applicant (Nov 26, 2026) - model meeting the bench: modeled the pitch axis as a transfer function; prediction matched the bench. Be ready to explain it in an interview.
- CONFIRMED by applicant (Nov 26, 2026) - why EE: 200-300 mV spikes on the 3.3V rail during SD writes; a moving-average filter only added lag; fixed with a 0.1 uF decoupling cap at the altimeter, a 10 uF bulk cap at the SD module, and a rerouted ground. Applicant says this is "mostly" why they chose EE.
- CONFIRMED by applicant (Nov 26, 2026) - diagnosis: derivative term reacting to IMU noise and kicking the motors; fixed by light filtering plus a lower derivative gain.
- Build order: "Months earlier" assumes the telemetry board (Spring/Summer) came before the gimbal (Summer/Fall). Fix if wrong.
- Opening scene (clean compile, nudging the mount, pitch swinging harder) and the tuning method ("changing one value at a time").
- "Beyond what my FLC courses covered": assumes no FLC course you took taught Laplace transforms, transfer functions, or stability margins.
- Orbital sim: "Last summer" assumes the sim was built during or after your Summer 2026 Differential Equations with Linear Algebra course.
- Shashine: "learned to bring engineers the test log that reproduced a bug." Fallback if not true: "troubleshot edge-case bugs with senior engineers and organized testing logs for internal tooling."
- "Finishing the calculus-based physics sequence": confirm on ASSIST that Physics 411/421/431 is the full sequence for your campuses. Physics 421, 431, and ENGR 400 are Spring 2027 plans only.
- Read the final aloud and rewrite any line that does not sound like you. UC requires you to certify the PIQs are your own work.
