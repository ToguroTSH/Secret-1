# Confirmed Details (applicant-supplied, Nov 26, 2026)

Used by: [[uc-writer]], [[uc-humanizer]], [[uc-auditor]]. These are real details the applicant gave after V3. Any future rewrite MUST keep them; never regenerate the PIQs from the original beat sheets alone.

## Required Major-Prep
- Gimbal: raw IMU + high derivative gain -> fast jitter/buzzing. A heavy low-pass filter stopped the buzz, but its phase lag caused slow swings that grew when the mount was nudged. Fixed by a lighter filter and a lower derivative gain.
- Telemetry board: 200-300 mV p-p spikes on the 3.3V rail and sensor line whenever the ESP32 wrote a burst to the SD card. A software moving-average filter only added lag to the 50Hz readings. Fix: 0.1 uF ceramic decoupling cap next to the altimeter power/ground pins, 10 uF bulk cap near the SD module, shortened/rerouted ground so SD writes stopped sharing the sensor's return path. Ripple dropped to about 20-30 mV (scope baseline).
- Why EE ("mostly" the reason): wanted to understand circuits, power delivery, and signal integrity to fix hardware at the source instead of patching data in code.
- Model: moment of inertia from mount weight + caliper measurements; servo torque/response specs from datasheet; bench step-response test for damping and delay. Predicted ~10-15% overshoot, ~0.4 s settling; bench ~15-20%, ~0.5 s.
- Courses: ENGR 420 = Statics; ENGR 400 (Spring 2027) = Intro to Electrical Circuits; CISP 360 = Intro to Structured Programming in C++; CISP 400 = Object-Oriented Programming in C++; PHYS 411 = Mechanics of Solids and Fluids; PHYS 421 = Electricity & Magnetism; PHYS 431 = Heat, Light, Modern Physics; CHEM 400 = General Chemistry I.

## Leadership
- All scenes and quotes in the V3 final are true (grill cook quotes, callouts ignored for weeks, call-ahead agreement, he stopped yelling).
- Training drill: new hires rang practice orders and watched their tickets reach the line. The modifier that kept getting missed: "no onions".
- Outcome: new hires ran the front counter through Friday rushes without the applicant stepping in.

## Community
- Arduino workshop in Aspen Hall FL1-130, a few weeks before the Tech Summit: a first-time builder's photoresistor + micro servo light tracker; Serial Monitor readings were clean, but the servo twitched and locked up on every upload; they were about to delete their code. The applicant sat down with a multimeter and had them trace the servo's current return. The servo ran off a 4-AA pack (to avoid browning out the Arduino) with no ground tied to the Arduino's GND. The applicant explained common ground ("voltage only means something relative to a shared zero"); they ran one jumper from battery negative to GND. The servo tracked their phone flashlight. They said, "Wait, that's it? One wire?", stayed 30 minutes late tuning thresholds, and signed up for a Tech Summit team that night.
- Attendance: 12 to 18 students per session (applicant-confirmed).

## Voice preferences (applicant feedback)
- Avoid stacking many 3-4 word dramatic sentences back to back; it reads "like a LinkedIn post." Combine them into normal sentences.
- Avoid "formalize"-style abstractions and neat colon lists of three.
- Prefer plain statements like "I want upper-division classes in signals, controls, and circuits so I can learn the theory behind the bugs I've been running into."
