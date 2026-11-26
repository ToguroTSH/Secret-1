# Required Major-Prep PIQ - v1
Prompt: Please describe how you have prepared for your intended major, including your readiness to succeed in your upper-division courses once you enroll at the university.

The code compiled cleanly. The gimbal still would not settle. On the bench at the FLC Innovation Center, my STM32 microcontroller read the IMU, a motion sensor, and drove both axes of my thrust-vectoring test stand. Every time I nudged the mount, pitch swung past level, came back, and swung harder.

I had designed the stand in Fusion 360 and 3D-printed its mounts. Holding it steady meant writing a PID loop, code that keeps correcting toward a target angle. My first gains were guesses. Across more than 15 bench tests in C++, I changed one value at a time and logged the response. The swing meant the derivative term was reacting to sensor noise, so I filtered the IMU signal before tuning again. To understand why it oscillated, I taught myself Laplace transforms and stability margins, beyond FLC's curriculum.

That habit started with math. After Calc 3 and Differential Equations with Linear Algebra this summer, I built an orbital simulator in Python and C++ that models 2-body transfers and atmospheric drag with 4th-order Runge-Kutta, a step-by-step method for solving motion equations. My first orbits drifted. I checked each run against published textbook benchmarks until the numbers matched.

I laid out a telemetry board in KiCad, circuit-board design software, combining an ESP32, a barometric altimeter, and an SD logger. I soldered through-hole and surface-mount parts, wrote C++ firmware that samples at 50Hz, and used FLC lab oscilloscopes to trace noise in the signal.

At Shashine Technologies, I wrote Python scripts that automated data validation and ran QA test cases. In weekly standups with senior engineers, I learned to show up with the test log that reproduced an edge-case bug before asking for help.

Upper-division circuits, signals, and controls courses will ask me to model a system, build it, and explain why the two disagree. I have done that on my own bench, with my own mistakes. This spring I will take Physics 421 and ENGR 400 to finish my preparation. I am ready for labs where the first test fails, because that is where I have learned the most.

Word count: 348

Sub-clauses answered:
- How you have prepared for your intended major -> paragraphs 1-5: gimbal PID build, self-studied controls, RK4 orbital simulator built on Calc 3 and Diff Eq/Linear Algebra, KiCad telemetry board, Shashine internship.
- Readiness to succeed in upper-division courses -> final paragraph: names upper-division circuits, signals, and controls work, ties it to the model-build-explain loop already practiced, names Spring 2027 Physics 421 and ENGR 400 as upcoming only.

Facts to verify with applicant:
- Opening scene: the gimbal oscillating with growing pitch swings after a clean compile, and nudging the mount to test it.
- Cause and fix: that the derivative term was amplifying IMU noise and that you filtered the IMU signal before retuning. Swap in the real cause and fix if different.
- "Changed one value at a time and logged the response" as your tuning method.
- "My first orbits drifted" and checking each run against benchmarks until they matched.
- "Show up with the test log that reproduced an edge-case bug before asking for help" as the standup lesson.
- The self-studied controls topics (Laplace, transfer functions, stability margins) come from Activity #20; the beat sheet assigns "self-studied controls" to this PIQ, but the Barrier beat sheet also mentions self-directed FEA/controls. FEA was left out here; make sure the Barrier PIQ does not repeat the controls detail.
