# Required Major-Prep PIQ - FINAL
Prompt: Please describe how you have prepared for your intended major, including your readiness to succeed in your upper-division courses once you enroll at the university.

When I first powered up my thrust-vectoring test stand, the servos buzzed. My STM32 fed raw IMU data into a C++ PID loop, and the high derivative gain turned every spike of sensor noise into jitter. I added a heavy low-pass filter and the buzzing stopped, but now whenever I nudged the mount, pitch swung past level and came back harder. The filter's lag made the loop unstable.

I had seen this months earlier on a telemetry board I laid out in KiCad with an ESP32, an altimeter, and an SD logger. On a Folsom Lake College (FLC) lab oscilloscope, the 3.3V rail spiked 200 to 300 mV whenever the ESP32 wrote to the SD card. A moving-average filter in firmware only added lag and could not stop the spikes from corrupting reads. So I fixed the board with a 0.1 uF decoupling capacitor at the altimeter, a 10 uF bulk capacitor at the SD module, and a rerouted ground. Ripple dropped to about 20 to 30 mV, near the scope's baseline.

That board taught me to ask which layer a problem lives in. The gimbal's problem was in the control loop, so I taught myself Laplace transforms and transfer functions and modeled the pitch axis. I estimated the mount's moment of inertia from its weight and caliper measurements, took servo specs from the datasheet, and ran a step-response test for damping and delay. With a light filter and a lower derivative gain, the model predicted 10 to 15 percent overshoot and about 0.4 seconds to settle. The bench showed 15 to 20 percent and 0.5 seconds, close enough to tell me which way to tune over 15+ tests.

All of this ran on coursework I have finished or am finishing: Calculus 3, Differential Equations with Linear Algebra, two semesters of C++, and mechanics and statics this fall. My gap is circuits, so this spring I am taking Electrical Circuits and Electricity and Magnetism. I want upper-division signals, controls, and circuits so I can learn the theory behind the bugs I have been running into on my own.

Word count: 348

Facts (applicant-confirmed, Nov 26, 2026; interview prep):
- Gimbal sequence: raw IMU + high derivative gain -> jitter; heavy low-pass filter stopped the buzz but its phase lag caused growing swings; fixed with a lighter filter and lower derivative gain.
- Telemetry board: 200-300 mV p-p spikes on the 3.3V rail during SD writes; moving-average filter only added lag; 0.1 uF decoupling cap at the altimeter, 10 uF bulk cap at the SD module, rerouted ground; ripple down to about 20-30 mV.
- Model inputs: moment of inertia from mount weight and caliper measurements, servo datasheet specs, bench step-response test for damping and delay. Predicted 10-15% overshoot / ~0.4 s settling; measured 15-20% / ~0.5 s.
- Coursework: Calc 3 and Differential Equations with Linear Algebra (Coastline, Summer 2026); CISP 360 (Los Rios, Summer 2026) and CISP 400 (Fall 2026, in progress) = two semesters of C++; PHYS 411 mechanics and ENGR 420 statics (Fall 2026, in progress). Spring 2027 planned: ENGR 400 Intro to Electrical Circuits, PHYS 421 Electricity & Magnetism.
- Cut from this essay for space (still in Activities): orbital simulator (#6), Shashine internship (#1).
- Interview prep: be ready to explain why a heavy filter's phase lag destabilizes a PID loop, and how you estimated the plant from the step response.
- Integrity: read this aloud and rewrite any line that does not sound like you before submitting.