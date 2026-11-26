# UC Transfer PIQ Vault - Project Brain

## Mission
Build a top-1% UC Transfer application for an Electrical Engineering transfer from Folsom Lake College (3.97 GPA; targets UC Berkeley, UCLA, UCSD, plus UC Davis, UC Irvine, UCSB): 1 Required Major-Prep PIQ + 3 Optional PIQs (#1 Leadership, #4 Barrier, #6 Community), each 325-350 words, plus 20 Activities & Awards entries of 350 characters or fewer.

## Directory map
- `00-context/` - applicant data: [[courses-and-majors]], [[activities-list]], [[piq-beat-sheets]], [[voice-sample]]
- `01-research/` - [[winning-patterns]]
- `02-critique/` - [[committee-review]] (v1 teardown + final re-score)
- `03-drafts/` - v1 and v2 drafts: `piq-required-major-v1/v2`, `piq-opt-1-leadership-v1/v2`, `piq-opt-4-barrier-v1/v2`, `piq-opt-6-community-v1/v2`
- `04-final/` - [[piq-required-major]], [[piq-opt-1-leadership]], [[piq-opt-4-barrier]], [[piq-opt-6-community]], [[uc-activities-350char]], [[AUDIT-REPORT]]
- `.claude/agents/` - uc-researcher, uc-writer, uc-admissions-critic, uc-humanizer, uc-auditor (one isolated context per phase)
- `.claude/skills/humanizer/` - humanizer skill used by uc-humanizer
- `.claude/skills/uc-*` - older single-session skills from the first setup; the agent pipeline below replaces them

## Pipeline
research -> 4 parallel v1 drafts -> committee critique -> 4 parallel v2 drafts -> 4 parallel humanizer passes -> final audit + 20 activities -> critic re-score of finals.

## Conventions
- Use Obsidian [[wikilinks]] (like [[piq-beat-sheets]]) when referencing other files in the vault.
- Never edit, delete, or touch the hidden `.obsidian/` folder.

## Strict word cap
Every PIQ is 325-350 words. Count the essay body only, with a script (PowerShell: `($body -split '\s+' | Where-Object { $_ }).Count`), never by eye. Print `Word count: N` at the bottom of every draft.

## Strict voice rule
Study [[voice-sample]] for sentence rhythm: concrete scene or dialogue openings, blunt short sentences mixed with reflective beats, specific numbers, plain words, admitted doubt, grounded directness, and an earned short takeaway. NEVER reuse the meditation, BrighterMinds, Arjun, cross-country, or Nikhil stories (or Coach Esayas, box-breathing, panic attacks) in any draft.

## Fact guardrails (all agents)
- Today is Nov 26, 2026. Spring/Summer 2026 courses are completed, Fall 2026 is in progress, Spring 2027 is planned (see [[courses-and-majors]]). Never claim the applicant has taken or used Physics 421, Physics 431, Chem 401, ENGR 312, ENGR 400, or ENGL C1000. These may appear only as upcoming coursework.
- Use only facts and numbers in `00-context/`. Elevate real work to its sharpest defensible framing. Never invent organizations, titles, awards, metrics, or outcomes.
- Scene details and dialogue not in the data must be listed under "Facts to verify with applicant" at the bottom of each draft so the applicant can confirm them or swap in what really happened.
- Each story's evidence belongs to one PIQ only (see the table in [[piq-beat-sheets]]).
- Integrity: UC requires applicants to certify the PIQs are their own work. Remind the applicant to read every final aloud and rewrite any line that doesn't sound like them before submitting.

## Final format
Plain ASCII text in the essay body: straight quotes, no smart quotes, no em-dashes (at most one plain hyphen-dash per essay), no markdown inside the body.

## Usage coaching
Drafting, critique, and humanizing run on Opus; research runs on Sonnet. Use `/clear` or a new session between big phases if running steps by hand. All progress lives in the files.
